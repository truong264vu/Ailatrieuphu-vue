
<template>
  <div id="start">
      <meta name="viewport" content="width=device-width, initial-scale=1">
      <!-- <div class="tutorial">
          <p>Chúng tôi có tất cả 15 câu hỏi .<br>
          Bạn có : <br>
          - 30 giây để trả lời mỗi câu hỏi <br>
                    - 2 quyền trợ giúp <br>
                   - 1 quyền dừng chơi</p>
      </div> -->
     
      <div class="startGame">
            
            <input type="submit" id="OnStart" value="Bắt đầu" @click="START_TIME()" @mousedown.once="hideScreenStart()">         
      </div>
       
  </div>
</template>

<script>
import { mapMutations } from 'vuex';
// import { mapGetters } from 'vuex'

export default {
    name: 'StartPlay',
    methods: {...mapMutations(['START_TIME']),
        hideScreenStart() {
            document.getElementById("OnStart").onclick = function () {
                document.getElementById("start").style.display = 'none';
            };      
          
        },
           
    }
        
    
}
</script>

<style scoped>
    #start .startGame {
         width: 1890px;
          height: 880px;
        background: url(../../images/dolar.jpg) no-repeat ;
        background-size: 100% 100%;
    }
    .hide{
        display: none;
    }
    #start .startGame input {
          position: absolute;
          font-size: 30px;
          background: rgb(69, 138, 218);
          color: rgb(231, 245, 244);
          left: 42%;
          top: 46%;
          height: 100px;
          width: 15%;
          border: 5px solid rgb(235, 232, 238);
          border-radius:40px ;
          font-weight: 1000;
    }
    #start .startGame input:hover {

        background: rgb(43, 101, 167);
        cursor: pointer;
    }

    @media (max-width: 1600px) {


    #start .startGame {
        width: 1600px;
        height: 880px;
        background: url(../../images/dolar.jpg) no-repeat ;
        background-size: 100% 100%;
    }
        #start .startGame input {
          left: 42%;
          top: 60%;
          height: 90px;
          width: 15%;
          border: 3px solid blueviolet;
          border-radius:40px ;
    }
    }

    @media (max-width: 1400px) {


    #start .startGame {
        width: 1400px;
        height: 880px;
        background: url(../../images/dolar.jpg) no-repeat ;
        background-size: 100% 100%;
    }
        #start .startGame input {
          left: 42%;
          top: 60%;
          height: 90px;
          width: 14%;
          border: 3px solid blueviolet;
          border-radius:40px ;
    }
    }

    @media (min-width: 900px) and (max-width: 1100px) {

    #start .startGame {
        width: 1100px;
        height: 880px;
        background: url(../../images/dolar.jpg) no-repeat ;
        background-size: 100% 100%;
    }
        #start .startGame input {
          left: 40%;
          top: 60%;
          height: 90px;
          width: 20%;
          border: 3px solid blueviolet;
          border-radius:40px ;
    }
    }

    @media (max-width: 900px) {
        #start {
            width: 900px;
            height: auto;
        }
    #start .startGame { 
        width: 900px;
        height: 354px;
        background: url(../../images/dolar.jpg) no-repeat ;
        background-size: 900px 400px;
        border: 5px solid black;

    }
        #start .startGame input {
          left: 40%;
          top: 60%;
          height: 70px;
          width: 20%;
          border: 3px solid blueviolet;
          border-radius:40px ;
          background: rgb(83, 59, 187);
    }
    }

</style>
