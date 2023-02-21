<template>
<div>
  <h2>Hello h2</h2>
  <New-element @addElement="newEl($event)"></New-element>
  <ElementGrid :elements="elements"
                @deleteEl="deleteIt($event)"></ElementGrid>

  
</div>
</template>
<script>
import ElementGrid from './components/ElementGrid.vue'
import NewElement from './components/NewElement.vue'

export default {
  data(){
    return{
      maxElements:10,
      elements :[
        'Element 1'
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
  
  components:{ElementGrid, NewElement}
}
</script>
<style>
body{
  background-color: bisque;
}

</style>
