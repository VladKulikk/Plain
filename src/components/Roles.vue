<template>
  <div class="main">
    <img :src="require(`@/${icon}`)" :alt="title">
    <h3>{{title}}</h3>
    <p>{{ text }}</p>
    <slot/>
  </div>
</template>

<script>
export default {
  name: 'RouteComponent',
  props: {
    icon: String,
    title: String,
    text: String
  }
}
</script>

<style scoped>
.main {
  display: flex;
  flex-flow: column;

  width: 40%;
}

img {
  width: 100px;
  height: 100px;
}

h3{
  font-weight: 400;
  font-size: 30px;
  line-height: 34px;
}
</style>