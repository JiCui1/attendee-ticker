<template>
  <div id="app">

    <main>
      <Title :maxPeople="20" :currentPeople="people" id="title_comp"/>
      <ButtonComp @upPeople="up" @downPeople="down" id="btns"/>
      <img src="./assets/person.png">
      <div id="blur_div"></div>
    </main>
    <div class="cir_container">
      <div id="big_cir"></div>
      <div id="small_cir"></div>
    </div>
  </div>
</template>

<script>
import Title from './components/Title.vue'
import ButtonComp from './components/ButtonComp.vue'

export default {
  name: 'App',
  components: {
    Title,
    ButtonComp
  },
  data(){
    return{
      people:0
    }
  },
  methods:{
    up(){
      if(this.people<20){
      this.people += 1
      }
    },
    down(){
      if(this.people>0){
        this.people -=1
      }
    }
  }
}
</script>

<style>
#app {
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  width: 100%;
  height: 100vh;
  background-color:#F8FAFB;
  display:flex;
  justify-content: center;
  align-items: center;
}

img{
  position:absolute;
  z-index: 20;
  top: 7rem;
  right: -3rem;
  height:14rem;
}
#title_comp{
  position:relative;
  z-index: 3;
  }
#btns{
  position:relative;
  z-index: 3;
  margin-top:-7rem;
}

.cir_container{
  position:absolute;
  left:0;
  top:0;
  width: 100%;
  height: 100vh;
  overflow: hidden;
}

#big_cir{
  position:absolute;
  left:-20rem;
  top:-20rem;
  width:40rem;
  height:40rem;
  border-radius: 50%;
  background-color: #045de9;
  background-image: linear-gradient(315deg, #045de9 0%, #09c6f9 74%);
}

#blur_div{
  position:absolute;
  width: 100%;
  height: 100%;
  background-color:rgba(255, 255, 255, 0.544);
  backdrop-filter: blur(10px);
  z-index: 2;
}

#small_cir{
  position:absolute;
  right:2rem;
  bottom:1rem;
  width:15rem;
  height:15rem;
  border-radius: 50%;
  background-color: #045de9;
  background-image: linear-gradient(315deg, #045de9 0%, #09c6f9 74%);
}

main{
  position:relative;
  z-index: 10;
  background-color:rgba(255, 255, 255, 0);
  width: 80%;
  height:80%;
  border-radius: 2rem;
  display:flex;
  flex-direction: column;
  justify-content: space-evenly;
  -webkit-box-shadow: 0px 4px 11px 5px rgba(19, 97, 242, 0.1); 
  box-shadow: 0px 4px 11px 5px rgba(19,97,242,0.1);
  overflow: hidden;
}
</style>
