<template>
    <div>
        <label>Title</label>
        <p>{{post.title}}</p>
        <br/>
        <label>Body</label>
        <p>{{post.body}}</p>
        <br/>
        <label>User Id</label>
        <br/>
        <p>{{post.userId}}</p>
        <hr/>
        <br/>
        <button @click='$emit("enlarge-text", 0.1)'>Enlarge Text!</button>
        <br/>
        <button @click='$emit("decrease-text", 0.1)'>Decrease Text Size!</button>
        <br/>
        <br/>
    </div>
</template>

<script>
export default {
    name: 'Comments',
    props: ['post'],
}
</script>

<style>

</style>
