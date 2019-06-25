<template>
    <div>
        <p>{{ post.title }}</p>
        <p>{{ post.body}}</p>
        <p>{{ post.userId }}</p>
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
