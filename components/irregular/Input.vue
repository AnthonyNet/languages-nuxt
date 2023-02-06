<template>
    <div>
        <p>{{title}}</p>

    
        <input class="border-4 inputPokus" type="text" @input="valueChanged">
    </div>
</template>

<script>
import myData from "../../myData/IrregularVerbs.js";

    export default {
        props: {
            title: String,
            number: Number
        },
         methods: {
            valueChanged(e){
            this.$emit('udalost', e.target.value);
          
    }
}
}

</script>

<style lang="scss" scoped>

</style>