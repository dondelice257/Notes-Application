<template>
    <div>
        <h1>Add Elements here</h1>
        <textarea name="" id="" required placeholder="Enter your text here..." v-model="element" cols="30" rows="10">

        </textarea>
        <button @click="newElement">Add New</button>
        <br>
        <span style="background:rgb(50, 150, 150); color : white; padding:3px">Click on the element in order to remove it </span>

    </div>
</template>

<script>

export default{
    data(){
        return{
            element : ''
        }
    },
    methods:{
        newElement(){
           
             if(this.element!=''){
                this.$emit('addElement', this.element);
            this.element=""
             }
             else{
                alert('The field cannot be empty')
             }
          
           
        }
    }
    
}
</script>
<style scoped>
div{
    display: flex;
    flex-direction: column;
    align-items:center;
    justify-content: center;
    text-align: center;
    margin-top: -70px;
 
}
button{
    padding: 10px;
    font-size: 18px;
    border: none;
    background: blue;
    color: rgb(255, 255, 255);
}
textarea{
    border: 2px solid blue;
}
</style>
