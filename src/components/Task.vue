<template>
<div @dblclick="$emit('toggle-reminder', task.id)" :class="[task.reminder ? 'reminder' : '', 'task']">
    <h3>{{task.text}}</h3>
    <i @click="$emit('delete-task', id)" class="fas fa-times"></i>
    <p>{{task.day}}</p>
</div>
</template>

<script>
export default{
    name: 'Task',
    props: {
        task: Object
    },

    
}

</script>

<style>
.fas {
  color: whitei;
  position: absolute;
  left:850px;
}
.task {
  background: rgb(158, 182, 158);
  margin: 5px;
  padding: 10px 20px;
  cursor: pointer;
}
.task.reminder {
  border-left: 5px solid green;
}
.task h3 {
  display: flex;
  align-items: center;
  justify-content: space-between;
}
</style>