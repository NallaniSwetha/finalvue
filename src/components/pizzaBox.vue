<template>
   
    
    <div v-for="pizza of pizzaStore" :key="pizza.price" >
       <SinglePizza :pizza=pizza />

    </div>

</template>
<script>
import SinglePizza from './SinglePizza.vue'

export default {
    name: 'pizzaBox',
    props:{
        pizzaStore: Array
    },
    components:{
        SinglePizza
    }
    
}
</script>
<style>

</style>
