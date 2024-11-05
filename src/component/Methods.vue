<template>
   <div class="relative text-center uppercase font-bold text-[20px] bg-green-400 py-2" v-on:mouseover="testmethod">this is a methods</div>
   <div>{{ testmethods }}</div>
</template>
<script>
export default{
    data(){
        return{
            testmethods:""
        }
    },methods:{
        testmethod(){
            this.testmethods="this is a testing methods"
        }
    }
}

</script>