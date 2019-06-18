<template>
    <div>
        <p>Add todos below, click to delete.</p>
        <input
        v-on:keyup.enter='addTodo'
        v-model='newTodo'
        class='todo'>
            <ul v-if='todos.length'>
                <li v-for='(n, index) in todos'
                :key='index'
                @click='removeTodo'>
                {{ n }}
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
        }
    },
    methods: {
        addTodo: function() {
            this.todos.push(this.newTodo)
            this.newTodo = ''
            return
        },
        removeTodo: function() {
            this.todos.splice(this.todos.index, 1)
            document.window.alert('Todo removed!')
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
