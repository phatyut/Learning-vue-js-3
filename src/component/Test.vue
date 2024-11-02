<template>
    <button v-on:click="clickme">click</button>
  <div class="w-[100px] h-[100px] bg-blue-600" :style="{fontSize:size}" v-show="font">Test</div>
</template>
<script>
export default{
  data(){
    return{
      size:'60px',
      font:false

    }
  },methods:{
    clickme(){
      alert("what is your name");
      this.font=true
      

    }
  }
}

</script>