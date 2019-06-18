<template>
    <div>
        <p>Add todos below, click to delete.</p>
        <input
        @keyup.enter='addTodo'
        v-model='newTodo'
        class='todo'>
            <ul v-if='todos.length'>
                <li v-for='(n, key) in todos'
                :key='key'
                @click.prevent='removeTodo(key)'>
                {{ n.name }}
                </li>
            </ul>
            <p v-else>No tasks available, get to work!</p>
    </div>
</template>

<script>
export default {
    name: "simpleTodo",
    data() {
        return {
            todos: [],
            newTodo: '',
            count: 0
        }
    },
    methods: {
        addTodo: function() {
            this.todos.push({name: this.newTodo, id: this.count})
            this.newTodo = ''
            this.count += 1
            return
        },
        removeTodo: function(index) {
            this.todos.splice(index, 1)
            return
        }
    }
}
</script>

<style lang='sass' scoped>
    input
        border: 2px black double
    .todo
        margin-bottom: 20px
    div
        font-size: 30px
    li
        font-size: 50px
</style>
