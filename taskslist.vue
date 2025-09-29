<template>
  <ul>
    <TaskItem 
      v-for="task in tasks" 
      :key="task.id" 
      :task="task" 
      @remove="removeTask"
    />
  </ul>
</template>

<script>
import TaskItem from './TaskItem.vue'

export default {
  name: 'TaskList',
  components: { TaskItem },
  props: {
    tasks: Array
  },
  methods: {
    removeTask(taskId) {
      this.$emit('remove-task', taskId)
    }
  }
}
</script>

<style scoped>
ul {
  list-style: none;
  padding: 0;
}
</style>
