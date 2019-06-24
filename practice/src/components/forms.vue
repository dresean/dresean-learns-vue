<template>
    <div class="container">
        <div>
            <label for='rick_owens'>Rick Owens</label>
            <input
            v-model='checked'
            type='checkbox'
            id='rick_owens'
            @click='handleCheck'
            value='Rick Owens'>
            <label for='jw'>J.W. Anderson</label>
            <input
            v-model='checked'
            type='checkbox'
            id='jw'
            @click='handleCheck'
            value='J.W. Anderson'>
            <label for='greg_lauren'>Greg Lauren</label>
            <input
            v-model='checked'
            type='checkbox'
            id='greg_lauren'
            @click='handleCheck'
            value='Greg Lauren'>
            <label for='craig_green'>Craig Green</label>
            <input
            v-model='checked'
            type='checkbox'
            id='craig_green'
            @click='handleCheck'
            value='Craig Green'>
        </div>
        <span>{{ checked }}</span>
        <br/>
        <br/>
        <hr/>
        <label for=''>True</label>
        <input type='radio'
        id='true'
        v-model='selected'
        value='true'/>
        <br/>
        <label for='false'>False</label>
        <input type='radio'
        v-model='selected'
        id='false'
        value='false'/>
        <br/>
        <span>{{ selected }}</span>
    </div>
</template>

<script>
export default {
    name: 'Forms',
    data() {
        return {
        checked: [],
        selected: [],
        count: 0
        }
    },
    methods: {
        handleCheck: function () {
            console.log(this.checked)
        },
    }
}
</script>

<style>

</style>
