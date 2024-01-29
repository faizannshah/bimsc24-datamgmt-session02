<!-- the script is where the js code goes -->
<script setup>
import { ref} from "vue" 

//Define variables and functions
let count = ref(0);
let user = ref("Faizan")
let text = ref("")
let newtext = ref("")


//fuctions that mutate and trigger updates
function increment() {
    count.value++
    console.log(count)
}

function addtext() {
text.value = newtext.value;
}
</script>

<!-- the template is where the html code goes -->
<template>

<div id="navbar" class="container"> 
        <div id="title">DataMgmt Assgn02 {{user}} </div>

</div>

<div id="flex">
     <div id="Sidebar1" class="container">
        Input your text here:
        <input v-model="newtext" type="text" placeboholder="Add text">
        <button @click="addtext">Update Text</button>
    </div>



  <div id="Main" class="container"> 
  
    {{ newtext }}
    

</div>
</div>

<button @click="increment"> Count is: {{ count }}</button>
<h2>{{name}}</h2>


</template>





<!-- style is where the css code goes -->
<style scoped>



html{
    
    background-color: black;
    background-image: url(https://github.com/iaac-macad/bimsc24-bootcamp-s2-demo/blob/main/cow.jpg?raw=true);
    color: rgb(0, 255, 174);
}

body{

    margin:0;
    
}

div{

    box-sizing: border-box;
}

#navbar{

    height: 50px;

}

#flex{

    display: flex;
    height: calc(100vh - 50px);

}

#Sidebar{
    width: 30%;
}

#Main{
    width:70%;

}
    .container{

        border-style: dotted;
        border-color: rgb(201, 16, 16);
        border-width: 5px;
    }
</style>