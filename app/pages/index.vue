<template>
<div class="h-[500px] w-[1200px] m-[50px] bg-neutral-800 flex flex-col gap-[20px] justify-center items-center">

    <div v-gsap.from="{
    x:100,
    duration:3,
    ease:'power2.inOut',
}" class="h-[50px] w-[50px] bg-blue-600 rounded-[10px]"></div>

    <div v-gsap.from="{
    x:150,
    duration:3,
    ease:'power2.inOut',
}", v-gsap.to="{x:300,duration:3,ease:'power2.inOut'}" class="h-[50px] w-[50px] bg-red-600 rounded-[10px]"></div>

    <div class="h-[50px] w-[50px] bg-green-600 rounded-[10px]"
    v-gsap.whenVisible.once.from="{opacity:0,x:-100}"
    ></div>
</div>
</template>

<script setup lang="ts">

</script>

