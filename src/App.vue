   <template>
   <div class="hdrWrap">
      <div class="hdr">
        <h2 v-for="(a,i) in menu" :key="(a,i)" @click="PageOn=[false,false,false];PageOn[i]=true;">{{a}}</h2>
      </div>
   </div>
   <Chars v-if="PageOn[0]==true"/>
   <Couple v-if="PageOn[1]==true"/>
   <Doolstagram v-if="PageOn[2]==true"/>
  </template>


<script>  
import data from './assets/data.js';
import Banner from './components/Banner.vue';
import Chars from './components/Chars.vue';
import Couple from './components/Couple.vue';
import Doolstagram from './components/Doolstagram.vue'

export default {
  name: 'App',
  data(){
    return{
      PageOn: [true,false,false],
      menu : ['캐릭터','커플투표','둘스타그램'],
      chars : data,
      modal : true,
      ind: 0,
    }
  },
  components: {
    Banner : Banner,
    Chars,
    Couple,
    Doolstagram,
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0;
}
img{
  width: 200px;
}
div{
  margin-top: 40px;
}
.lightBox{
  background-color: rgba(0,0,0,0.5);
  width: 100vw;
  height: 100vh;
  position: fixed;
  top: 0;left: 0;
  margin-top: 0;
}
.contain{
  width: 40%;
  height: 45%;
  overflow: hidden;
  margin: auto;
  position: absolute;
  top: 0;bottom: 0;left: 0;right: 0;
}
.contain>button{
  position: absolute;
  top: 0;
  right: 0;
  font-size: 30px;
}
.hdrWrap{
  background-color: aquamarine;
  margin-top: 0;
}
.hdr{
  display: flex;
  width: 60%;
  max-width: 500px;
  margin: 0 auto;
  justify-content: space-between;
}
.hdr h2{
  cursor: pointer;
  font-size: 15px;
  line-height: 20px;
}
</style>
