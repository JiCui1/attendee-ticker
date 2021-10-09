<template>
    <div>
        <h1>Attendee Ticker</h1>
        <p>Max people allowed is <span>{{maxPeople}}</span>, Currently we have:</p>
        <h2>{{currentPeople}}</h2>
    </div>
</template>

<script>
export default {
    name:"Title",
    props:{
        currentPeople: Number,
        maxPeople: Number
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@300&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;700&display=swap');
*{
    margin:0;
    padding:0;
}
h1{
    font-family: 'Poppins', sans-serif;
    font-weight: 700;
    font-size:5rem;
    color:black;
}

span{
    font-weight: 700;
    color: #1361F2
}

p{
    font-family: 'Poppins', sans-serif;
    font-weight: 300;
    color:black;
}

h2{
    font-family: 'Poppins', sans-serif;
    font-size: 8rem;
    color: #1361F2
}

</style>