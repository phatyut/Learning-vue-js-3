<template>
        <div class="text-center text-green-400 bg-gray-400 py-5 font-bold text-[20px] hover:bg-yellow-300 " v-show="showbox">
                <button v-on:click="show">SHOW FOR NOTES</button>
        </div>
        <div class="w-full h-auto bg-gray-300 text-white border-b-4 border-black rounded-[5px]" v-show="mainbox">
            <button v-on:click="hide" v-show="hidebox"
                class="bg-white text-black absolute left-2 top-1 px-5 font-bold rounded-[5px] hover:bg-gray-400 hover:text-pink-500">
                    hide
            </button>

    <!-- this is a one block the end -->

            <div class="flex justify-center items-center flex-col" >
                <div class="border-[3px] p-2 border-black flex justify-center flex-col items-center" >
                    <div>click event animation</div>
                    <div><button v-on:click="restultclick++">click</button></div>
                    <div>{{ restultclick }}</div>
                </div>
            </div>
    <!-- this is a two block the end -->
            
           <div class="relative" 
                v-on:mousemove="testbackgroundcolor=Math.floor(Math.random() * 100)" 
                v-bind:style="{backgroundColor:'hsl('+testbackgroundcolor+',50%,50%)'}">
                <div>
                    <div class="w-[300px] h-72 relative"></div><br>
                  
                   
                </div>
           </div>
        </div>
 
</template>
<script>
export default{
    data(){
        return{
            showbox:false,
            hidebox:true,
            mainbox:true,

            restultclick:0,    

            testbackgroundcolor:100,
          
            
        }
    },methods:{
        show(){
            this.mainbox=true;
            this.showbox=false;
            this.hidebox=true
        },hide(){
            this.hidebox=false
            this.showbox=true
            this.mainbox=false
        }
      
    }
}
</script>