<!--
<template>
  <div class="list">
    <ul>
      <li v-for="(n, index) in constants(words)"
      :key="index"
      >
      {{ n }}
      </li>
    </ul>
  </div>
</template>

<script>
   export default {
    data(){
      return {
      words: ["geeks", "for", "unbrella", "geeks", "a", "portal", "bacon", "to", "learn", "can", "be", "computer", "science", "zoom", "yup", "apple", "fire", "in", "be", "data", "geeks", "alpha"]
      }
    },
    methods: {
      constants: function (words) {
        return words.filter(function (word) {
          switch(word[0]) {
            case "a":
              return null
              break
            case "e":
              return null
              break
            case "i":
              return null
              break
            case "o":
              return null
              break
            case "u":
              return null
              break
            default:
              return word
              break
          }
        })
      }
    },
  }
</script>

<style lang='sass' scoped>
  .list
    font-size: 50px
    text-align: left
    margin: 10px
    padding-left: 30px
</style>

--> 

<template>
  <div>
    <template>
      <ul>
        <li
        v-for='n in todoList'
        v-if='!n.completed'
        >
        {{ n.todo }}
        </li>
      </ul>
    </template>
    <template>
        <ul v-if='newTodos.length > 0'>
          <hr/>
          <li v-for='n in newTodos' id='new'>{{ n }}</li>
        </ul>
          <p v-else>No new todos!</p>
    </template>
  </div>
</template>

<script>
export default {
    data() {
      return {
        todoList: [
          {todo: 'call mom', completed: false},
          {todo: 'call dad', completed: true},
          {todo: 'feed cat', completed: true},
          {todo: 'walk dog', completed: false},
          {todo: 'cook dinner', completed: false},
          {todo: 'do laundry', completed: true},
          {todo: 'clean room', completed: true},
        ],
        newTodos: ['thing']
      }
    }
}
</script>

<style lang='sass' scoped>
  li
    text-align: left
    margin: auto
    font-size: 50px
  ul
    padding-left: 10%
  #new
    color: green
</style>
