<template>
    <div class="btn_container">
        <h3 @click="callUpEmit">+</h3>
        <h3 @click="callDownEmit">-</h3>
    </div>
</template>

<script>
export default {
    name:"ButtonComp",
    methods:{
        callUpEmit(){
            this.$emit("upPeople")
        },
        callDownEmit(){
            this.$emit("downPeople")
        }
    }
}
</script>

<style>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;700&display=swap');
.btn_container{
    display:flex;
    justify-content: space-around;
}

h3{
    font-family: 'Poppins', sans-serif;
    font-weight: 400;
    width:2rem;
    font-size:1.5rem;
    height: 2rem;
    background-color:#1361F2;
    border-radius: 50%;
    color:white;
    display:flex;
    justify-content: center;
    align-items: center;
    cursor: pointer;
    -webkit-box-shadow: 0px 4px 11px 1px rgba(19,97,242,0.4); 
    box-shadow: 0px 4px 11px 1px rgba(19,97,242,0.4);
}

</style>