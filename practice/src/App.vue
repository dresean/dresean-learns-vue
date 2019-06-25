<!--
<template>
  <div id="app">
      <keyboardEvents/>
    <Forms />
    <MoreForms />
    <div :style='{fontSize: postFontSize + "em"}'>
    <BlogPost
    v-for='post in fetched'
    :post='post'
    :key='post.id'
    @enlarge-text='postFontSize += 0.1'/>
    </div>
  </div>
</template>

<script>

// import keyboardEvents from './components/keyboardEvents.vue'
import Forms from '@/components/forms.vue'
import MoreForms from '@/components/moreForms.vue'
import BlogPost from '@/components/BlogPost.vue'

export default {
  name: 'app',
  components: {
    // keyboardEvents,
    // Forms
    // MoreForms
    BlogPost
  },
  data() {
    return {
      posts: [
            {title: 'A Title', id: 1},
            {title: 'Another Title', id: 2},
            {title: 'Another-nother title', id: 3},
            {title: 'Who guessed this would be a title?', id: 4},
            {title: 'You win, a title', id: 5},
            {title: 'Not a title in public', id: 6},
        ],
        fetched: [],
        postFontSize: 1
    }
  },
  methods: {
    'enlarge-text': function () {

    }
  },
  created: function (){
    let vm = this
    fetch('https:jsonplaceholder.typicode.com/posts')
    .then(response => {
      return response.json()
    })
    .then(data => vm.fetched = data)
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
-->

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
<!--
<template>
  <div id='app'>
    <div :style='{fontSize: postFontSize + "em"}'>
      <Comments v-for='post in posts'
      :post='post'
      @enlarge-text='postFontSize += $event'
      @decrease-text='onTextDecrease'
      :key='post.id'/>
    </div>
  </div>
</template>


<script>
import Comments from '@/components/comments.vue'

export default {
  name: 'app',
  components: {
    Comments
  },
  data() {
    return {
      postFontSize: 1,
      posts: []
    }
  },
  methods: {
    onTextDecrease: function(decreaseValue) {
      this.postFontSize -= decreaseValue
    }
  },
  created: function () {
    let vm = this
    fetch('https://jsonplaceholder.typicode.com/posts')
    .then(response => response.json())
    .then(data => vm.posts = data)
  }
}
</script>

<style>

</style>
-->

<template>
  <div id='app'>
    <br/>
    <label>Custom Input</label>
    <br/>
    <CustomInput v-model='searchText' />
  </div>
</template>

<script>
import CustomInput from '@/components/customInput.vue'

export default {
  name: 'app',
  components: {
    CustomInput
  },
  data() {
    return {
      searchText: ''
    }
  }
}
</script>

<style>

</style>
