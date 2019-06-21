<!-- <template>
    <div>
        <button @click.prevent='greet'
        >Greet</button>
    </div>
</template>

<script>
export default {
    name: "events",
    data() {
        return {
            name: "Dre'Sean"
        }
    },
    methods: {
        greet: function (event) {
            alert('Hello ' + this.name)
            if(event) {
                alert(event.target.tagName)
            }
        }
    }

}
</script>

<style lang='sass' scoped>
    button
        font-size: 750px
</style>
-->

<!--
<template>
    <div>
    <button @click.prevent='warn("you clicked the warning button bro!", $event)'>Warning</button>
    </div>
</template>

<script>
export default {
    name: 'events',
    methods: {
        warn: function (message, event) {
            if(event) {
                event.preventDefault()
                alert(message)
            }
        }
    }
}
</script>

<style lang='sass' scoped>
    button
        font-size: 500px
        border: 20px black dashed
</style>
-->

<!-- above uses the DOM event listener to acheive an alert message-->