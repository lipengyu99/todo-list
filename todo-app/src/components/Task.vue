<template>
    <transition name="fade">
    <div class="task" v-if="!task.deleted">
        <label for="id">{{task.title}}</label>
        <transition name="fade">
            <span 
            class="task_delete"
            v-show="task.done"
            @click="deleteTask({task})"
            >
            <i class="fa fa-trash"></i>
            </span>
        </transition>
    </div>
    </transition>
</template>

<script>
import { mapMutations } from "vuex";
let GID = 1
export default {
    props:{
        task:{
            type:Object,
            require:true
        }
    },
    data() {
        return {
            id:`task-${GID++}`
        }
    },
    methods: {
        ...mapMutations(['deleteTask'])
    },
}
</script>

<style lang="scss">

</style>
