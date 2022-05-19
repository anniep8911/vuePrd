<template>
<form>  
  <textarea name="" id="" cols="30" rows="10"></textarea><br>
  <input type="submit" value="글올리오">
</form>
<div v-for="a in msg" :key="a">
    <img src="../assets/pic2.jpg" alt="">
    <p>{{a}}</p>
</div>
</template>

<script>
export default {
    name:'Doolstagram',
    data(){
        return{
            msg :['외로운 둘리는 귀여운 아기공룡'],
        }
    }

}
</script>

<style>

</style>