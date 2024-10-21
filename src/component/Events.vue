<template>
    <!-- <div class="relative w-full flex flex-col items-center justify-center">
        <div class="relative border-black border-[2px] border-dotted flex flex-col justify-center overflow-hidden items-center rounded-[5px] ">
            <img src="../images/boy.jpg" alt="" class="w-[200px]">
            <div class="uppercase">this is a counter <span class="text-red-400 font-bold underline">{{ counter }}</span></div>
            <button v-on:click="incrementCounter"  
             class="relative border-[2px] border-blue-400 rounded-[5px] bg-red-500 text-white border-dotted p-[5px] font-extrabold">
                click me
            </button>
        </div>
    </div> -->
    <div>
    <button @click="incrementCounter">Click me</button>
    <p :class="{'text-red-600':isRed,'text-yellow-500':yellow}"> Click count: {{ counter }}</p>
  </div>
</template>
<script>
export default{
    data(){
        return{
            counter:0,
            isRed:false,
            yellow:false
        }
    },methods:{
       
    incrementCounter() {
      this.counter++;
      if (this.counter === 3) {
        this.isRed = true;
      

    }else if(this.counter===4){
        this.yellow=true
    }
  
       
    }
}
}
</script>