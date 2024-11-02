<template>
    <div class="text-center text-green-400 bg-gray-400 py-5 font-bold text-[20px] hover:bg-yellow-300" v-show="showbox">
            <button v-on:click="show">SHOW FOR NOTES</button>
    </div>
    <div class="w-full h-[300px] bg-black text-white" v-show="mainbox">
        <button v-on:click="hide" v-show="hidebox"
             class="bg-white text-black absolute left-1 top-1 px-5 font-bold rounded-[5px] hover:bg-gray-400 hover:text-pink-500">
                hide
        </button>

<!-- this is a one block -->

        <div class="flex justify-center items-center flex-col" >
            <div class="border-[1px] border-white flex justify-center flex-col items-center" v-bind:style="{'background-color':bg ? 'red' : 'none'}">
                <div>click event animation</div>
                <div><button v-on:click="counterresult">click</button></div>
                <div>{{ restultclick }}</div>
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
        },counterresult(){
            this.restultclick++;
            if(this.restultclick >= 0 && this.restultclick <=5){
                this.bg=true

            }

            
        }

    }
}
</script>