<template>
    <div class=" text-black by-2 border-red-500 flex flex-col border-[2px] ">
        <div class="text-white bg-blue-300 text-center underline text-[40px]">This is a for loops in vue js</div>
        <div class="relative flex justify-center flex-row items-center  ">
            <div v-for="counter in images" class="relative bg-blue-400  border-[2px] border-red-500 rounded-[20px] overflow-hidden h-[400px]">
                <img :src="counter.img" alt="boy" class="relative w-[200px]">
                <div class="text-center underline text-red-400">{{ counter.name }}</div>

            </div>
        </div>      
    </div>
</template>
<script>
import Boy from '../images/boy.jpg'
import Dog from '../images/dog.jpeg'
export default{
    data(){
        return{
            images:[
                {img:Boy,name:'this is a Boy'},
                {img:Dog ,name:'this is a dog'}
            ]
        }
    }
}
</script>