<script setup lang="ts">
import {ref} from 'vue'
import{ScrollTrigger} from 'gsap/ScrollTrigger'
onBeforeMount(()=>{
    useGSAP().registerPlugin(ScrollTrigger)
})

const section1=ref()

const animation=()=>{
    gsap.to('.Dot-1',{
        width:'100vw',
        ease:'power2.inOut',
        scrollTrigger:{
            trigger:'#main',
            start:'30% top',
            end:'50% 10%',
            scrub:1,
            markers:false,
        }
    })
}
</script>

<template>
<div>
    <section v-gsap.timeline.pinned class="w-[100vw] h-[200vh] flex justify-center items-center" id="main" >
    <h1
    v-gsap.add.fromTo="[{opacity:0, y:50},{opacity:1, y:0}]"
    v-gsap.add.to="{opacity:1,y:-50}"
    class="Dot-1">Hello World</h1>
    
    
    
</section>
</div>


</template>



<style scoped>
.style-text{
    opacity: 0;
    font-size: 100px;
    color: #2A2A2A;
    align-items: center;
    font-weight: 900;
}
.Dot-1{
   font-size: 60px;
   color: #2A2A2A;
   align-items: center;
   font-weight: 900;
}
</style>