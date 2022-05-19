<template>
   <div v-for="(a,i) in chars" :key="(a,i)">
      <img :src="a.image" alt="">
      <h4>이름 : {{a.name}}</h4>
      <h4>나이 : {{a.age}}세</h4>
      <p>특징: {{a.content}}</p>
      <button @click="modal=false; ind = i;">{{a.name}} 영상보기</button>
    </div>

    <div class="lightBox" v-if="modal==false">
      <div class="contain">
        <iframe width="560" height="315" :src="chars[ind].video" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
        <button @click="modal=true">X</button>
      </div>
    </div>
</template>

<script>
import data from '../assets/data.js';

export default {
    name:'Chars',
    data(){
    return{
      chars : data,
      modal : true,
      ind: 0,
    }
  },
}
</script>

<style>

</style>