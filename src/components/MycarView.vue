<template>

    <div :class="car.Isused ? 'Blue': 'red' ">
        <h2>{{car.carname}}</h2>
        <div class = "ED2">
            <p>
                <ul>
                    <li><b>Specifications</b></li>
                    &nbsp;&nbsp;<u>Year of manufacture:</u> {{car.year}}<br>
                    &nbsp;&nbsp;<u>transmission:</u> {{car.transmission}}<br>
                    &nbsp;&nbsp;<u>drivetrain:</u> {{car.drivetrain}}<br>
                    &nbsp;&nbsp;<u>color:</u> {{car.color}}<br>
                </ul>
            </p>
        </div>
    </div>
</template>

<script>

export default{
    name: 'MycarView',
    props:{
        car: Array
    }  
}
</script>

<style scoped>



h4{
    margin: 2px;
}

div{
    background-color: #E7F2F8;
    color: black;
    padding: 1em;
}

.red{
    background-color: #74BDCB !important;

}
.Blue{
    background-color: #FFA384 !important;
}


</style>