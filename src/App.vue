<template>
  <div class="p-0 m-0 box-border">
    <div class="relative flex flex-col">
      <div><Note/></div><br><br>
      <div><Bind/></div><br><br>
      <div><For/></div><br><br>
      <div><Events/></div><br><br>
      <div><Methods/></div><br><br>
      <div><Test/></div><br><br>
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