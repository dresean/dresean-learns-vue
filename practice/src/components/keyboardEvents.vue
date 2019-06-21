<template>
    <div
    class='container'
    @keyup.shift.tab.prevent='handleShiftTab'>
        <p>Add a todo below!</p>
        <input
        v-model='newTodo'
        @keyup.esc.exact='handleEsc'
        @keyup.enter='handleSubmit'
        />
        <p v-if='empty'>You must type in something to do that!</p>
        <ul v-if='todoList.length'>
            <li
            v-for='(n, key) in todoList'
            @click.left.exact='removeTodo(key)'
            :key='key'>
            {{ n.name }}
            </li>
            <p v-if='visible'>{{ n.createdAt }}</p>
        </ul>
        <p v-else>Nothing to do yet! Get to work!</p>
        <p>Key:
            <br/>
            press <code>enter</code> to add the todo.
            <br/>
            press <code>right mouse button</code> to view the deadline for the todo.
            <br/>
            press <code>left mouse button</code> on the todo to delete the todo.
            <br/>
            press <code>Esc</code> to clear the current input
            <br/>
            press <code>Shift + Tab</code> to add the todo.
            <br/>
        </p>
    </div>
</template>

<script>
export default {
    name: 'keyboardEvents',
    data() {
        return {
            message: 'You found the secret treasure! You will receive a raise in 120 days!',
            newTodo: '',
            todoList: [],
            showAlert: false,
            count: 0,
            empty: false,
            visible: false
        }
    },
    methods: {
        handleSubmit: function () {
            if(!this.newTodo.length) return this.empty = true
            const date = new Date().toDateString()
            this.todoList.push({name: this.newTodo, dateCreated: date, id: this.count})
            this.newTodo = ''
            this.count += 1
            this.empty = false
        },
        removeTodo: function (key) {
            this.todoList.splice(key, 1)
        },
        handleEsc: function () {
            this.newTodo = ''
        },
        handleShiftTab: function () {
            alert(this.message)
        },
    },
}
</script>

<style lang='sass' scoped>
    .container
        font-size: 30px
    input
        border: 5px black double
        padding: 10px
        margin: 30px
    li
        font-size: 55px
        color: red
        margin: auto
        padding: 1px
        list-style-type: none
    ul
        margin: 0px
        padding: 0px
</style>

<!--
create a todo list
if you right click on the todo, view the tool tip showing the time to be completed - 
if you left click on the todo, remove the todo - 
press enter to submit the todo - 
press escape to clear the currently typed todo - 
press shift and tab to display an alert
-->