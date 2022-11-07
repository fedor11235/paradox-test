<template>
  <categories-item 
    title="Обязательные для трудоустройства" 
    suptitle="Документы, без которых невозможно трудоустройство человека на какую бы то ни было должность в компании вне зависимости от гражданина"
  />
  <categories-item />
  <categories-item />
</template>

<script>
import СategoriesItem from './components/СategoriesItem.vue'

export default {
  name: 'App',
  components: {
    'categories-item': СategoriesItem
  }
}
</script>

<style sccoped>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
