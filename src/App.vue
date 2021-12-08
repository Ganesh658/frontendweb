<template>
  <div class="container">
    <!-- #3 must use the component-->
    <Header covidvacName="Covid Vaccines" 
      />


    <COVID :covidvaccines="covidvaccines"  />




  </div>
</template>
<script>



//import HelloWorld from './components/HelloWorld.vue'
// 1
import Header from './components/Header.vue'
import COVID from './components/CovidVbox.vue'



export default {
  name: 'App',
  components: {
    // 2 register the component 
    Header,
    COVID
  },

  data(){
    return {
      covidvaccines:[
        {

        }
      ]
    }
  },
  methods: {
    // promises

      async fetchvac(){
        

        
  
         
         const res= await fetch('https://covivac.herokuapp.com/api')

         const data= await res.json()
         console.log(data)
         return data
      }

  },

  async created(){
    this.covidvaccines = await this.fetchvac()
  }
}
</script>










<style>


@import url('https://fonts.googleapis.com/css2?family=Montserrat:wght@300&display=swap');
* {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  font-family: 'Montserrat', sans-serif;
}
.container {
  max-width: 600px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
}

div{
  margin-bottom: 0.5em;
}



</style>


