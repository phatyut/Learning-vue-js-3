<template>
  <div class="p-0 m-0 box-border">
    <div class="relative flex flex-col space-y-5 px-1">
      <div><Note/></div>
      <div><Bind/></div>
      <div><For/></div>
      <div><Events/></div>
      <div><Methods/></div>
      <div><Test/></div>
    </div>
   
    
  </div>
  </template>



<script>
import Note from './component/Note.vue';
import For from './component/For.vue';
import Bind from './component/Bind.vue';
import Events from './component/Events.vue';
import Methods from './component/Methods.vue';
import Test from './component/Test.vue';


export default{
  components:{Note,Bind,For,Events,Methods,Test},
  data(){
    return{

    }
  }
}
</script>