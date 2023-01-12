<script>

</script>

<template>
    <div>
    <form @submit="addToDo">
      <input type="text" v-model="title" name="title">
      <button type="submit">Add</button>
    </form>
  </div>
</template>