<template>
    <h1> {{StoreName}} </h1>
</template>

<script>

  export default{
    name: 'MyHeader',
    props:{
        StoreName:String,
    }
  }
</script>

<style>
h1{
    color: aliceblue;
    text-align: center;
}

</style>