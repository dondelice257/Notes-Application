<template>
<div>
 
  <NewElement @addElement="newEl($event)"></NewElement>
  <ElementGrid :elements="elements"
                @deleteEl="deleteIt($event)"></ElementGrid>

  
</div>
</template>
<script>
import ElementGrid from './components/ElementGrid.vue'
import NewElement from './components/NewElement.vue'3

export default {
  data(){
    return{
      maxElements:10,5
      elements :[
        'just first element'
      ]
    }
  },
  methods:{
    newEl(el){
      this.elements.push(el);
      
      },
      deleteIt(index){
       this.elements.splice(index, 1)
      }

    },
  
  components:{ElementGrid,
              NewElement
  }
}
</script>
<style>
body{
  background-color: bisque;
}

</style>
