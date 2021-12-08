<template>
    

    <div :class="covidvac.inmarket ? 'green': 'red' ">

     <h2>{{covidvac.name}}</h2>
    <h4> {{covidvac.year}}</h4>

    <h4>Effectiveness : {{covidvac.effectiveness}}</h4>
    
    



    </div>
    


</template>

<script>
// book -- covidvac
export default{
    name: 'CovidVaccine',
    props:{
        covidvac: Object
    }
}
</script>

<style scoped>



h4{
    margin: 0px;
}

div{
    background-color: green;
    color: black;
    padding: 1em;
    
}

.red{
background-color: grey;

}


</style>