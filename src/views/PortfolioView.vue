<template>
  <div>
    <h2>Portfolio Page</h2>
    <div class="repos">
      <div class="column" v-for="project in data" :key="project.id">
        
         <repo-component
            :title='project.name'
            :html_url="project.html_url"
            :imageSrc="require(`../assets/images/${project.name}.png`)"
            :id="project.id" />
      </div>
    </div>
  </div>
</template>

<script>
import RepoComponent from '../components/RepoComponent.vue'
import githubService from "../services/GithubService";

export default {
  data() {
    return {
      data: null,
    };
  },
  components: {
    RepoComponent
  },

  mounted() {
    githubService.getRepos().then((response) => {
      this.data = response.data.filter((project) => {
        return (
          project.name === "vue2-practice" ||
          project.name === "API-practice-vanilla-javascript" ||
          project.name === "CSS-practice"
        );
      });
    });
  },
};
</script>

<style scoped>
.repos {
  display: flex;
  justify-content: space-around;
}

.column {
  margin: 20px;
}
</style>