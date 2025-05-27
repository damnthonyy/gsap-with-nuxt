<script setup lang="ts">
import {ref} from 'vue'
import{ScrollTrigger} from 'gsap/ScrollTrigger'
onBeforeMount(()=>{
    useGSAP().registerPlugin(ScrollTrigger)
})

const section1=ref()

onMounted(()=>{

})
</script>

<template>
<section v-gsap.timeline class="w-[100vw] h-[200vh] flex justify-center items-center" ref="section1">
    <section class="flex justify-center items-center">
        <div class="w-[400px] h-[400px] bg-neutral-600 rounded-full mt-[50px] absolute" v-gsap.markers.timeline.pinned="{start:'top 40%',end:'50% 10%'}" >  <!-- scoll-a scoller-start scroll-b scroller-end -->
            
        </div>
    </section>
    
</section>

</template>



<style scoped>
.style-text{
    opacity: 0;
    font-size: 100px;
    color: #2A2A2A;
    align-items: center;
    font-weight: 900;
}

</style>