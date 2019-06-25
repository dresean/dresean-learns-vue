<template>
    <div>
        <p>{{ post.title }}</p>
        <p>{{ post.body}}</p>
        <p>{{ post.userId }}</p>
        <button @click='$emit("enlarge-text")'>Enlarge Text</button>
    </div>
</template>

<script>
export default {
    name: 'BlogPost',
    props: ['post'],
}
</script>

<style>

</style>
