<template>
  <div class="main">
    <img :src="require(`@/${img}`)" :alt="title">
    <div class="listArea">
      <h2>{{ title }}</h2>
      <ul>
        <li v-for="item in items" v-bind:key="item"
            :style="`list-style-image: url(${require(`@/assets/${listIndicator}.svg`)})`">
          {{ item }}
        </li>
      </ul>
    </div>
  </div>
</template>

<script>
export default {
  name: 'ServiceComponent1',
  props: {
    img: String,
    title: String,
    listIndicator: String,
    items: Array,
  }
}
</script>

<style scoped>
.main {
  display: flex;
  flex-flow: row;
  justify-content: space-between;

  margin: 100px 0;
}

.listArea {
  display: flex;
  flex-flow: wrap;
  justify-content: center;
  align-items: center;

  padding: 50px 0;

  width: 40%;
}

li {
  color: rgba(0 0 0 / 60%);
  font-weight: 400;
  line-height: 24px;

  margin: 20px 0;
}

h2 {
  font-weight: 400;
  font-size: 38px;
  line-height: 44px;
}

</style>
