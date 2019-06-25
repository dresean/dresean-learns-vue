<!--
<template>
    <div>
        <label for='a'>A</label>
        <input type='checkbox' v-model='toggle' true-value='A' false-value='no'/>
        <label for='b'>B</label>
        <input type='checkbox' v-model='toggle' true-value='B' false-value='no'/>
        <label for='c'>C</label>
        <input type='checkbox' v-model='toggle' true-value='C' false-value='no'/>
    </div>
</template>

<script>
export default {
    name: 'MoreForms',
    data() {
        return {
            toggle: ''
        }
    },
    watch: {
        toggle(value) {
            console.log('toggle changed!', this.toggle)
        }
    }
}
</script>

<style>

</style>
-->

<!--
<template>
    <div>
        <label for='D'>D</label>
        <input type='radio' value='D' v-model='radioSelect' />
        <label for='E'>E</label>
        <input type='radio' value='E' v-model='radioSelect' />
        <label for='F'>F</label>
        <input type='radio' value='F' v-model='radioSelect' />
        <br/>
        <hr/>
    <span>You selected: {{ radioSelect }}</span>
    </div>
</template>

<script>
export default {
    name: 'MoreForms',
    data() {
        return {
            radioSelect: null
        }
    }
}
</script>

<style>

</style>
-->










<template>
    <div>
        <select v-model='selected'>
            <option v-for='option in options' :value='option.value' :key='option.value'>{{ option.name }}</option>
        </select>
        <hr/>
        <br/>
    <span>Selected: {{ selected }}</span>
    </div>
</template>

<script>
export default {
    name: 'MoreForms',
    data() {
        return {
            selected: null,
            options: [
                {name: 'Please Select an Option Below', value: null},
                {name: '456', value: 456},
                {name: '789', value: 789},
                {name: '101112', value: 101112},
                {name: '131415', value: 131415},
                {name: '161718', value: '161718'},
            ]
        }
       
    },
}
</script>

<style>

</style>

<!--
<template>
    <div>
        <select v-model='selected'>
            <option value='null' disabled>Please Select An Option Below</option>
            <option value='A'>A</option>
            <option value='B'>B</option>
            <option value='C'>C</option>
            <option value='D'>D</option>
        </select>
        <hr/>
        <br/>
        <span>{{ selected }}</span>
    </div>
</template>

<script>
    export default {
        name: 'MoreForms',
        data() {
            return {
                selected: 'null'
            }
        }
    }
</script>

<style>

</style>
-->