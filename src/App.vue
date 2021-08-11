<template>

  <div id="app">
  <meta name="viewport" content="width=device-width, initial-scale=1">

   <div class="win"><win /></div>
   <div class="bodyApp"><bodyApp /></div>
   <div class="start"><StartPlay /></div>
   <div class="rotate-screen"></div>

  </div>
</template>

<script>
import { mapState } from 'vuex'
import bodyApp from './components/bodyApp'
import win from './components/win'
import StartPlay from './components/StartPlay'
export default {
  name: 'App',
  components: { bodyApp , win , StartPlay},
  computed: 
    mapState(['count'])
  
}
</script>

<style>

#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  text-decoration: none;
  list-style: none;
  width: 100%;
  height: 100%;
  background-size: 100%;
  max-width: 1880px;
  max-height: 880px;
}
#app .win{
  position:absolute;
  z-index: 2;
}
#app .bodyApp{
  position:absolute;
  z-index:1;
}
#app .rotate-screen{
  position:absolute;
  z-index:4;
}
#app .start {
  position:absolute;
  /* top: -10px; */
  left: 8px;
  z-index: 3;
}

@media (min-width: 100px) and (max-width: 440px) {
    #app .rotate-screen {
      width: 100%;
      height: 100%;
      background: rgb(18, 37, 61) url(../images/rotatedevice.gif) no-repeat;
      background-size: 380px 850px;
    }
    #app .start {
      display: none;
}
    #app .win {
      display: none;
    }

}
@media (min-width: 440px) and (max-width: 600px) {
    #app .rotate-screen {
      width: 100%;
      height: 100%;
      background: black url(../images/rotatedevice.gif) no-repeat;
      background-size: 600px 850px;
     
    }
    #app .start {
      display: none;
}
      #app .win {
      display: none;
    }

}
</style> 