<template>
    <div class="cardetails">
        <div v-for="car in cars" :key="car.id" >     
               <MycarView :car="car"/>
        </div>
    </div>

</template>

<script>
import MycarView from "./MycarView.vue"
export default {
    name: 'MyCarDetails',
    components: {
        MycarView
    },
    props:{
        cars: Array

    } 
}
</script>


<style>
.cardetails{

    background-color: bisque;
    border: 5px solid #4C5270;
    padding: 1em;
    color: gray;
}

</style>