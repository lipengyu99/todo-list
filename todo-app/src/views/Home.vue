<template>
  <div class="home">
    <app-bar title="TODO" left="bars" right="search"></app-bar>
    <avatar/>
    <gradient/>
    <todo-list/>
  </div>
</template>

<script>
import AppBar from '../components/AppBar.vue'
import Avatar from '../components/Avatar.vue'
import Gradient from '../components/Gradient.vue'
import TodoList from '../components/TodoList.vue'
export default {
  components:{
    "app-bar":AppBar,
    "avatar":Avatar,
    "gradient": Gradient,
    "todo-list":TodoList,
  }
}
</script>

<style>
.home{
  height: 100%;
  width: 100%;
  overflow: hidden;
  color: white;
}
</style>
