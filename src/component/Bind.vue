<template>
    <div class="relative flex flex-col bg-gray-300 border-[5px] border-black ">
        <div class="text-[30px] text-red-600 font-bold text-center underline">This is a bind in vue js</div>
        <div class="relative w-full flex justify-center ">
            <img :src="inputimg" class="relative w-[20%] rounded-[20px]">
        </div>
        <div :class="['bg-red-400 text-center text-[20px]']" >Testing bind class in uve js</div>
    </div>
</template>
<script>
import imgs from '../images/boy.jpg'
export default{
 data(){
    return{
        inputimg:imgs
    }
 }
}
</script>