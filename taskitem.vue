<template>
  <li>
    <span>{{ task.title }}</span>
    <button @click="$emit('remove', task.id)">Remover</button>
  </li>
</template>

<script>
export default {
  name: 'TaskItem',
  props: {
    task: Object
  }
}
</script>

<style scoped>
li {
  display: flex;
  justify-content: space-between;
  margin: 5px 0;
  padding: 5px;
  background: #f0f0f0;
  border-radius: 4px;
}

button {
  background: #ff4d4f;
  color: white;
  border: none;
  padding: 2px 8px;
  border-radius: 4px;
  cursor: pointer;
}

button:hover {
  opacity: 0.8;
}
</style>
