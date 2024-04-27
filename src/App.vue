<template>

  <!--Step 3 use the component-->
  <MyHeader StoreName="Pizza Store"/> 
  <pizzaBox :pizzaStore=pizzaStore />
 
</template>

<script>
// Step: 1 Import the components
import MyHeader from './components/MyHeader.vue'
import pizzaBox from './components/pizzaBox.vue'


export default{
  name: 'App',

  // Step 2: Register the components
  components:{
    MyHeader,
    pizzaBox
  },
  data(){
    return {
      pizzaStore: []
    }
  },
  methods:{
    async fetchpizzaStore(){
      const res = await fetch('https://finalnodejs-emyn.onrender.com/api');
      const data = await res.json()
      console.log(data)
      return data
    }
  },
  async created(){
      this.pizzaStore = await this.fetchpizzaStore();
  }

}
</script>


<style>
body{
    background-image: url(pizza.jpg);
    background-size: cover;
    background-attachment: fixed;
    font-size: 20px;
    font-family:'Times New Roman', Times, serif;
}
</style>
