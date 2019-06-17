<!-- <template>
<div>
    <ul>
      <li v-for="(n, index) in startsWithConstant(words) key='index'> {{ n }} </li>
    </ul>
  </div>
</template>

<script>
export default {
  name: 'Hello',
  data () {
    words: ["geeks", "for", "unbrella", "geeks", "a", "portal", "bacon", "to", "learn", "can", "be", "computer", "science", "zoom", "yup", "apple", "fire", "in", "be", "data", "geeks", "alpha"]
  },
  methods: {
    startsWithConstant: function(words) {
      return words.filter(function (word) {
        switch(word[0].toLowercase()) {
          case "a":
            return word
            break
          case "e":
            return word
            break
          case "i":
            return word
            break
          case "o":
            return word
            break
          case "u":
            return word
            break
          default:
            return null
            break
        }
      })
    }
  }
}
</script>

<style>

</style> -->

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

