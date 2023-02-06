<template>
    <div>
        <Navbar />
       <Card title="[Oxford-B1]" />
    </div>
</template>

<script>
import Navbar from '~/components/navbar/Navbar.vue';
import Card from '../../components/card/Card.vue';
import OxfordB1 from '../../myData/OxfordB1.js';

export default{
    components:{
            Navbar,
            Card
        }
}
</script>

<style lang="scss" scoped>

</style>