<script>
export default {
    name: 'todoItem',
    data () {
      return {
        todos: [
            {
                id: 1, 
                title: "naam van todo",
                done: false
            },
            {
                id: 2, 
                title: "leuke todo",
                done: false
            }
        ]
      }
    }
}
</script>

<template>
    <li v-for="(item, index) in todos">
        <li class="item">{{ item.title }}</li>
    </li>
</template>