<template>
  <div id="win" v-bind="show()">
      <div v-show="count == questions.length">
        <img src="../../images/cup.jpg">
      </div>
      
  </div>
</template>

<script>
import { mapState } from 'vuex'
export default {
    name:'win',
    computed: mapState(['count','questions']),
    methods: {
        show() {
            var el = document.getElementById('win')
            if(this.$store.state.count == this.$store.state.questions.length){
                el.style.display = "block";
            }
        }
    }
    
        
    
}
</script>

<style >
#win {
    height: 880px;
    width: 1890px;
    display: none;
}
 #win img {
    height: 880px;
    width: 100%;
    
 }
@media (max-width:1600px )
{
    #win {
        width: 1600px;
        height: 880px;
    }
     #win img {
    width: 1600px;
    height: 880px;
    
 }
}
 
 @media (min-width:900px ) and (max-width:1200px )
{
    #win {
        width: 1200px;
        height: 880px;
    }
     #win img {
         width: 1200px;
        height: 880px;
    
 }
}
@media (max-width:900px )
{
    #win {
        width: 900px;
        height: 350px;
    }
     #win img {
    width: 900px;
    height: 350px;
    
 }
}

</style>