<template>
    <div class="mydata">
        <h3> {{pizza.name}}</h3>
        <h4> {{pizza.size}}</h4>
        <h4> {{pizza.toppings}}</h4>
        <h4> {{pizza.saucesForDipping}}</h4>
        <h4> {{pizza.price}}</h4>
    </div>
</template>

<script>

export default{
    name: 'SinglePizza',
    props:{
        pizza: Array
    }
}
</script>



<style>

h4{
    margin: 2px;
}

.mydata{
    background-color: rgb(207, 186, 169, 0.4) ;
    padding: 5px;
    border-radius: 10px;
    margin: 10px;
    border: 2px solid rgb(174, 174, 174);
}
</style>