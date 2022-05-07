<template>
  <div class = "container">
      <MyHeader titleName="Car Guru" 
        description="Get info about the cars and their specifications" />
      <MyCarDetails :cars="cars"/>
      <MyAbout About="About us"/>

  </div>
</template>

<script>
import MyHeader from './components/MyHeader.vue'
import MyCarDetails from './components/MyCarDetails.vue'
import MyAbout from './components/MyAbout.vue'



export default {
  name: 'App',
  components: {
    MyHeader,
    MyCarDetails,
    MyAbout
  },

  data(){
    return {
      cars: [],
      isHidden: false
    }
  },
  methods: {
    // promises

      async fetchCars(){
         const res= await fetch('https://pradeep-nodejs-backend.herokuapp.com/api')
         const data= await res.json()
          console.log(data, data.cars)
         return data.cars
      }

  },

  async created(){
    this.cars = await this.fetchCars()
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
.container {
  max-width: 600px;
  margin: 30px auto;
  overflow: auto;
  min-height: 300px;
  border: 0.3em solid black;
  padding: 30px;
  border-radius: 5px;
  background-color: #EFE7BC;
}

div{
  margin-bottom: 0.5em;
}
</style>
