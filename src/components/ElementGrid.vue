<template>
<div class="gen">
  <div class="contEl" @click="delet(index)" v-for="(element, index) in elements" :key="(element, index)">{{element}}</div>
</div>
</template>

<script>

export default {
  props:['elements'],
  methods:{
    delet(index){
      this.$emit('deleteEl', index)
      


    }
  }
  
}
</script>
<style scoped>
.contEl{
  background: rgb(190, 185, 185);
  color: rgb(0, 0, 0);
  border: 1px solid black;
  font-family: sans-serif;
  min-width: 140px;
  max-width: 200px;
  max-height: 100px;
  font-size: 25px;
  text-align: center;
  padding: 20px 0px 20px 0px;
  margin: 20px;
  display: flex;
  flex-direction: row;
  overflow-x: auto;
}
.contEl:hover{
  background: rgb(235, 135, 135);
}
textarea{
  display: flex;
  flex-wrap: wrap;
}
.gen{
  display: flex;
  flex-wrap: wrap;
  align-items: flex-start;
  
}

</style>
