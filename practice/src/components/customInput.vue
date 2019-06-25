<template>
    <div>
        <input
        :value='value'
        @input='$emit("input", $event.target.value)'
        placeholder='Please enter a phrase.'/>
    </div>
</template>

<script>
export default {
    name: 'CustomInput',
    props: ['value'],
}
</script>

<style>

</style>

<!-- 

-->