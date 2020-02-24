<template>
    <div class="gradient">
        <gradient-color
        v-for="(todo,index) in todos"
        :key="todo.name"
        :colors="todo.colors"
        :active="index <= currentIndex"
        >
    
        </gradient-color>
        
    </div>
</template>

<script>
import { mapState } from "vuex";
import GradientColor from './GradientColor.vue'
export default {
components:{
    "gradient-color":GradientColor
},
computed: {
    ...mapState(['todos','currentIndex'])
},
}
</script>

<style lang="scss">
.gradient{
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
    z-index: -1;
}
</style>
