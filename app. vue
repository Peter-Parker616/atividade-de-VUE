<template>
  <div id="app">
    <h1>Lista de Tarefas</h1>
    <input 
      v-model="newTask" 
      @keyup.enter="addTask" 
      placeholder="Digite uma nova tarefa..."
    />
    <button @click="addTask">Adicionar</button>

    <TaskList 
      :tasks="tasks" 
      @remove-task="removeTask"
    />
  </div>
</template>

<script>
import TaskList from './components/TaskList.vue'

export default {
  name: 'App',
  components: { TaskList },
  data() {
    return {
      newTask: '',
      tasks: []
    }
  },
  methods: {
    addTask() {
      if (this.newTask.trim() !== '') {
        this.tasks.push({ id: Date.now(), title: this.newTask })
        this.newTask = ''
      }
    },
    removeTask(taskId) {
      this.tasks = this.tasks.filter(task => task.id !== taskId)
    }
  }
}
</script>

<style scoped>
#app {
  max-width: 400px;
  margin: 0 auto;
  font-family: Arial, sans-serif;
}

input {
  width: 70%;
  padding: 5px;
  margin-right: 5px;
}

button {
  padding: 5px 10px;
}

h1 {
  text-align: center;
  margin-bottom: 20px;
}
</style>
