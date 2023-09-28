<template>
  <div class="hello">
    <a :href="html_url">
      <img class="repo-image" :src="imageSrc" alt="">
    </a>
    <p><a :href="html_url">{{  title }}</a></p>
    <p>{{  id }}</p>
  </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
    title: String,
    html_url: String,
    imageSrc: String,
    id: Number,
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}

.repo-image {
  width: 200px;
}
</style>
