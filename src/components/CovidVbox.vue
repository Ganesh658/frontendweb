<template>
    
     <div class="COVIDbody">
         
        <div v-for="covidvac in covidvaccines" :key="covidvac.id" >
                
                <COVIDV :covidvac="covidvac"/>
        </div>

        

     </div>

</template>

<script>

import COVIDV from "./Covid.vue"
export default{

    name: 'COVID',
    components: {
        COVIDV
    },
    props: {
        covidvaccines: Array
    }

}

</script>


<style>

.COVIDbody{

    background-color:pink;
    padding: 1em;
    color: gray;
}
</style>