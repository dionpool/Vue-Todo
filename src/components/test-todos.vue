<script>
export default {
    name: 'todos',
    data () {
      return {
        todoEntries: [
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
    <li v-bind:key="item.id" v-for="(item, index) in todoEntries">
        {{ item.title }}
    </li>
</template>