<script setup>
import { ref, onMounted, watch, computed, reactive } from 'vue'
import { useRouter } from 'vue-router'
const router = useRouter()
const optionList = ref(['HOME', 'ABOUT', 'MENU', 'GALLERY', 'CONTACT US'])
const showHamburger = ref(false)
const scrollTo = (id) => {
  if(menuShow.value){
    menuShow.value = false
  }
  console.log(id)
  const element = document.getElementById(id)
  console.log(element)
  if(element){
    const elementPosition = element.getBoundingClientRect().top;
    const offsetPosition = elementPosition + window.pageYOffset - 120;
    window.scrollTo({
      top: offsetPosition,
      behavior: 'smooth'
    });
  }
}
</script>
<template>
  <div class="flex bg-white pt-[22px] pl-[90px] pr-[90px] pb-[22px] justify-center items-center laptop:justify-center tablet:justify-center laptop:pt-[10px] laptop:pb-[10px] tablet:pt-[10px] tablet:pb-[10px] fixed top-0 left-0 z-50 w-full">
    <div class="flex justify-between items-center w-full desktop:max-w-[1000px] tablet:justify-center">
      <div class="flex items-center gap-[8rem]">
        <div class="flex items-end cursor-pointer" @click="router.push('/')">
          <img class="w-[127px] h-[75px]" src="@/assets/img/logo.png" alt="logo">
        </div>
        <div class="flex gap-[32px] text-black laptop:hidden tablet:hidden text-[15px]">
          <div v-for="(link, idx) in optionList" :key="idx" @click="scrollTo(item)" class="cursor-pointer">{{ link }}</div>
        </div>
      </div>
      <div class="text-white bg-[#4B3426] font-[500] px-[18px] py-[12px] rounded-full underline">ORDER ONLINE</div>
    </div>
    <img src="@/assets/img/menu.svg" class="absolute top-[16px] right-4 cursor-pointer desktop:hidden mac:hidden tablet:hidden" @click="showHamburger = true">
    <img src="@/assets/img/menuWhite.svg" class="absolute top-[16px] right-4 cursor-pointer desktop:hidden mac:hidden" @click="showHamburger = true">
  </div>
  <Transition name="slide-fade">
    <div class="w-full h-full fixed top-0 left-0 bg-white z-50 flex items-center pt-[75px] flex-col" v-if="showHamburger">
      <img src="@/assets/img/close.svg" class="fixed top-[16px] right-4 cursor-pointer desktop:hidden" @click="showHamburger = false">
      <div class="flex gap-[24px] text-text-black flex-col items-center">
        <NuxtLink v-for="(link, idx) in routerData" :key="idx + 'router'" :to="link.link">{{ link.linkName }}</NuxtLink>
      </div>
      <div class="rounded-[40px] w-[111px] h-[41px] bg-main-yellow flex items-center justify-center text-white font-normal mt-[24px]">
        <span>专业谘询</span>
      </div>
    </div>
  </Transition>
</template>
<style lang="scss" scoped>
.slide-fade-enter-active {
  transition: all 0.3s ease-out;
}

.slide-fade-leave-active {
  transition: all 0.3s ease-out;
}

.slide-fade-enter-from,
.slide-fade-leave-to {
  transform: translateX(20px);
  opacity: 0;
}
</style>
