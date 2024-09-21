<template>
  <div class="pt-[119px]">
    <div id="BANNER" class="h-[710px] relative">
      <img class="w-full h-full object-cover" src="@/assets/img/banner.png" alt="">
      <div class="absolute text-white left-[10%] top-[35%] flex flex-col gap-2">
        <div class="text-[2rem] font-[700]">Brew Memories in Park Slope! </div>
        <div class="flex flex-col">
          <div class="text-[1.5rem] font-[400]">Unforgettable Bubble Tea</div>
          <div class="text-[1.5rem] font-[400]">and Coffee in Brooklyn.</div>
        </div>
        <div class="bg-white px-[22px] py-[1rem] font-[500] text-black w-max h-[48px] rounded-full cursor-pointer mt-[1rem] underline">
          ORDER NOW
        </div>
      </div>
    </div>
    <div id="ABOUT" class="px-[12%] flex pt-[139px] pb-[239px] justify-evenly">
      <div class="w-[50%] flex flex-col items-center">
        <div class="w-[405px]">
          <div class="text-[2rem] font-[700] mb-[1rem]">WE ARE BREW<br> MEMORIES!</div>
          <div class="font-[400] mb-[71px] w-[405px]">
            Welcome to Brooklyn’s best café in Park Slope, where passion meets perfection in every cup. Dive into a world of aromatic brews, handcrafted from globally sourced beans, and expertly roasted here in New York’s beloved borough. 
          </div>
          <img class="w-[405px] h-[280px] mb-[75px]" src="@/assets/img/about1.png" alt="">
          <div class="text-[1.5rem] font-[700]">Freshly Made</div>
          <div class="font-[400]">Fresh coffee, quality drinks, excellent meals!</div>
        </div>
      </div>
      <div class="w-[50%] flex flex-col items-center">
        <div class="w-[405px]">
          <img class="w-[405px] h-[280px]" src="@/assets/img/about2.png" alt="">
          <div class="my-[84px] w-[405px]">
            We roast our coffee locally in small batches to ensure you get the freshest beans around. Not only is our coffee roasted to perfection, but all our drinks, including the finest bubble tea, as well as our meals and desserts, up hold the same standard of excellence!
          </div>
          <img class="w-[405px] h-[280px]" src="@/assets/img/about3.png" alt="">
        </div>
      </div>
    </div>
    <div id="MENU" class="flex flex-col justify-center items-center bg-[#4B3426] py-[100px] relative">
      <div class="flex flex-col justify-center items-center">
        <div class="font-[300] text-white">our delicious offer</div>
        <div class="text-[1.5rem] text-white">Unique food and charming spot in Brooklyn!</div>
      </div>
      <div class="flex justify-center gap-[10%] w-full my-[2rem]">
        <div class="flex flex-col items-center justify-center w-[250px]">
          <div v-for="(item, index) in menu1List" :key="index" class="w-full text-center">
            <div class="text-white py-[2rem]">{{ item }}</div>
            <div v-if="index !== menu1List.length - 1" class="w-full border-t border-dashed border-white" />
          </div>
        </div>
        <div class="flex flex-col items-center justify-center w-[250px]">
          <div v-for="(item, index) in menu2List" :key="index" class="w-full text-center">
            <div class="text-white py-[2rem]">{{ item }}</div>
            <div v-if="index !== menu2List.length - 1" class="w-full border-t border-dashed border-white" />
          </div>
        </div>
      </div>
      <div class="bg-white py-[12px] px-[24px] rounded-full cursor-pointer">Order Online</div>
      <img class="w-[450px] h-[320px] absolute top-[-25%] left-[20%]" src="@/assets/img/menu.png" alt="">
    </div>
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
const menu1List = ref<string[]>(['COFFEE', 'SPECIALTY LATTE', 'FRIZZY SPARKLING & SLUSH', 'FRESH FRUIT  TEA'])
  const menu2List = ref<string[]>(['SPECIAL SMOOTHIE', 'LEMONADE', 'FOOD'])
</script>

<style lang="scss" scoped>
</style>