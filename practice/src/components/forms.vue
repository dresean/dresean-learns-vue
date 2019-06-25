<!--
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
        <br/>
        <br/>
        <hr/>
        <br/>
        <br/>
        <select v-model="option" class='styling'>
            <option disabled value=''>Please select an option below</option>
            <option>A</option>
            <option>B</option>
            <option>C</option>
        </select>
        <br/>
        <br/>
        <span>{{ option }}</span>
        <br/>
        <br/>
        <hr/>
        <br/>
        <br/>
        <select v-model="selectMultiple" class='styling' multiple>
            <option disabled value=''>Please select a damn thing below</option>
            <option>D</option>
            <option>E</option>
            <option>F</option>
        </select>
        <br/>
        <br/>
        <span>{{ selectMultiple }}</span>
        <br/>
        <br/>
        <hr/>
        <br/>
        <br/>
        <select v-model="dynamicSelect" class='styling'>
            <option
            v-for='option in dynamicOptions'
            :key='option.value'
            v-bind:value='option.value'>
                {{ option.name }}</option>
        </select>
        <br/>
        <br/>
        <span>Selected: {{ dynamicallySelected }}</span>
    </div>
</template>

<script>
export default {
    name: 'Forms',
    data() {
        return {
        checked: [],
        selected: [],
        count: 0,
        selectMultiple: [],
        option: [],
        dynamicallySelected: 1,
        dynamicOptions: [
            {name: 'One', value:1},
            {name: 'Two', value:2},
            {name: 'Three', value:3},
            {name: 'About Tree Fiddy', value:4},
        ]
        }
    },
    methods: {
        handleCheck: function () {
            console.log(this.checked)
        },
    }
}
</script>

<style lang='sass' scoped>
    .styling
        border: 5px black double

</style>
-->


<template>
    <div>
        <select v-model='selected'>
            <option v-for='option in options' v-bind:value='option.value'><p>{{ option.name}}</p></option>
        </select>
        <span>Selected: {{ selected }}</span>
    </div>
</template>

<script>
export default {
name: 'Forms',
data() {
    return {
        selected: '1',
        options: [
            {name: 'one', value: '4'},
            {name: 'two', value: '3'},
            {name: 'three', value: '2'},
            {name: 'four', value: '1'},
        ]
    }
}
}
</script>

<style lang='sass' scoped>
    select
        border: 20px black double
        margin: auto
        padding: auto
    p
        font-size: 20px
        color: reen
</style>
