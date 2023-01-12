<script>
export default {
    name: 'addToDo',
    data() {
        return {
            title: ''
        }
    },
    methods: {
        addToDo(event){
            event.preventDefault();
        
            const newToDoObject = {
                id: todoEntries.length + 1,
                title: this.title,
                completed: false
            }
            
            this.$emit("add-todo-event", newToDoObject);
            this.title= '';
        }
    }
}
</script>

<template>
    <div>
    <form @submit="addToDo">
      <input type="text" v-model="title" name="title">
      <button type="submit">Add</button>
    </form>
  </div>
</template>