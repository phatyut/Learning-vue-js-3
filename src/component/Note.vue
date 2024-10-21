<template>
<div class=" w-full " :style="{hieght:hieght}" >
    <div class="relative bg-blue-400 overflow-hidden ">
        <div class="relative capitalize text-center text-yellow-400 font-extrabold text-[25px] underline ">noted tips in vue js </div>
        <button class="absolute top-0 right-0 bg-yellow-400 text-red-600 font-medium px-5 py-3 rounded-sm hover:bg-white hover:text-black" v-on:click="show" v-show="showbox">show</button>
        <button class="absolute bottom-0 right-0 bg-yellow-400 text-red-600 font-medium px-5 py-3 rounded-sm hover:bg-white hover:text-black z-10" v-on:click="hide" v-show="hidebox">hidden</button>
 <br>
       <div title="It's in box note tips" class="z-0">
<!-- random by clicked -->
            <div class="relative flex justify-center items-center ">
                <div class=" flex justify-center items-center flex-col bg-red-400 p-[10px] rounded-md">
                    <div class="text-center capitalize font-medium" :class="{'bg-blue-600':textblue,'bg-yellow-400':textyellow}">random by click</div>
                    <div class=" flex justify-center items-center ">
                        <button class="relative bg-gray-500 px-[10px] rounded-sm text-white font-nomal"
                        v-on:click="clickrandom">
                        click
                        </button>
                    </div>
                    <div class="text-center">{{ random }}</div>
                </div>
            </div>
<br>
<!-- mousemove to change background -->
            <div class="relative flex flex-col justify-center items-center">
                <div class="relative  bg-green-300 rounded-md px-5">
                    <div class="text-center capitalize font-medium"> mousemove to change background </div><br>
                    <div class="relative text-center underline font-[25px] capitalize ">
                        <div class="flex justify-center items-center flex-col">
                            <div class="relative w-[300px] h-[100px] border-red-500 border-[1px] border-double"
                                :style="{backgroundColor:'hsl('+changebackground+',60%,60%)'}"
                                v-on:mousemove="changebackground=Math.floor(Math.random()*1000)">
                            </div>
                            <div>{{ changebackground }},60%,60%</div>
                        </div>
                    </div>
                </div>
            </div>
<br>
        </div>
    </div>
</div>
</template>
<script>
export default{
    data(){
        return{
            random:0,
            textblue:false,
            textyellow:false,
            showbox:true,
            hidebox:false,
            changebackground:0,
            hieght:'50px'
            
        }
    },methods:{
        clickrandom(){
            this.random=Math.floor(Math.random()*10);
            if(this.random==2){
                this.textblue = true;
                alert("your are clicked to number two with blue text")
            }else if(this.random==4){
                this.textyellow=true;
                alert("your are clicked to number four with yellow text")
            }else{
                this.textblue=false;
                this.textyellow=false
            }
        },show(){
            if(this.show){
                this.hidebox=true;
                this.showbox=false;
                this.hieght=this.hieght==='50px' ? '400px' :'50px'
            }
        },hide(){
            if(this.hide){
                this.hidebox=false;
                this.showbox=true

            }
        }
    }
}
</script> 