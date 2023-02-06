<template>
    <div>
        <input class="border-4" type="text" @input="valueChanged">
    </div>
</template>

<script>
    export default {
        methods: {
            valueChanged(){
            console.log('value changed');
        },
        }
    }

</script>

<style lang="scss" scoped>

</style>