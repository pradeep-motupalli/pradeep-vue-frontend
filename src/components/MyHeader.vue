<template>
<div>
    <h1>{{titleName}}</h1>
    <h2>{{description}}</h2>
</div>
</template>

<script>
export default {
    name: 'MyHeader',
    props:{
        titleName: String,
        description:String
    }   
}
</script>

<style scoped>
div{
    text-align: center;
    border: 5px solid #4C5270;
    padding: 2px;
}
h1{
    color: #DB1F48;
}

</style>