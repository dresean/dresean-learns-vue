<template>
  <div id="app">
    <!-- <keyboardEvents/> -->
    <Forms />
  </div>
</template>

<script>

import keyboardEvents from './components/keyboardEvents.vue'
import Forms from '@/components/forms.vue'

export default {
  name: 'app',
  components: {
    keyboardEvents,
    Forms
  }
}
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>

<!--
<template>
  <div>
    <p>DANG</p>
  </div>
</template>

<script>
export default {

}
</script>

<style lang='sass' scoped>
  p
    font-size: 1000px
    word-wrap: wrap
    word-break: break-word
    hyphen: auto
    width: 100%
</style>
--> 