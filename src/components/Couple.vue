<template>
   <div v-for="(a,i) in people" :key="(a,i)">
      <h4>{{a}}❤{{animals[i]}}</h4>
      <h3>{{scroe[i]}}</h3>
      <button @click="scroeCount(i)">Vote</button>
      
    </div>
</template>

<script>
export default {
    name : 'Couple',
    data(){
        return{
            scroe:[0,0,0],
            people:['고길동','희동이','마이콜'],
            animals:['둘리','또치','도우너'],
        }
    },
    methods: {
        scroeCount : function(a){
            this.scroe[a]++;
        }
    },
}
</script>

<style>

</style>