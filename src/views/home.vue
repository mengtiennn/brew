<template>
  <div class="desktop:pt-[119px] tablet:pt-[95px]">
    <div id="HOME" class="h-[710px] tablet:h-[516px] relative">
      <img class="w-full h-full object-cover" src="@/assets/img/banner.png" alt="">
      <div
        class="w-full absolute text-white left-[10%] top-[35%] flex flex-col gap-2 tablet:items-center tablet:left-0 tablet:top-[10%]">
        <div class="text-[11px] font-[400] desktop:hidden tablet:mb-[1.5rem]">COZY PLACE. FRESH COFFEE.</div>
        <div class="text-[2rem] font-[700] tablet:w-[80%] tablet:text-center tablet:text-[32px] tablet:mb-[1.5rem]">Brew
          Memories in Park Slope! </div>
        <div class="flex flex-col tablet:text-center">
          <div class="text-[1.5rem] font-[400] tablet:text-[14px]">Unforgettable Bubble Tea</div>
          <div class="text-[1.5rem] font-[400] tablet:text-[14px]">and Coffee in Brooklyn.</div>
        </div>
        <div class="desktop:hidden w-[1px] h-[5rem] bg-white my-[1.2rem]" />
        <div
          class="bg-white px-[22px] py-[1rem] font-[500] text-black w-max h-[48px] rounded-full cursor-pointer mt-[1rem] underline"
          @click="goUrl()">
          ORDER NOW
        </div>
      </div>
    </div>
    <div id="ABOUT" class="px-[12%] flex pt-[139px] pb-[239px] justify-evenly tablet:pt-[72px]">
      <div class="w-[50%] flex flex-col items-center tablet:hidden">
        <div class="w-[405px]">
          <div class="text-[2rem] font-[700] mb-[1rem]">WE ARE BREW<br> MEMORIES!</div>
          <div class="font-[400] mb-[71px] w-[405px]">
            Welcome to Brooklyn’s best café in Park Slope, where passion meets perfection in every cup. Dive into a
            world of aromatic brews, handcrafted from globally sourced beans, and expertly roasted here in New York’s
            beloved borough.
          </div>
          <img class="w-[405px] h-[280px] mb-[75px]" src="@/assets/img/about1.png" alt="">
          <div class="text-[1.5rem] font-[700]">Freshly Made</div>
          <div class="font-[400]">Fresh coffee, quality drinks, excellent meals!</div>
        </div>
      </div>
      <div class="w-[50%] flex flex-col items-center tablet:hidden">
        <div class="w-[405px]">
          <img class="w-[405px] h-[280px]" src="@/assets/img/about2.png" alt="">
          <div class="my-[84px] w-[405px]">
            We roast our coffee locally in small batches to ensure you get the freshest beans around. Not only is our
            coffee roasted to perfection, but all our drinks, including the finest bubble tea, as well as our meals and
            desserts, up hold the same standard of excellence!
          </div>
          <img class="w-[405px] h-[280px]" src="@/assets/img/about3.png" alt="">
        </div>
      </div>
      <div class="desktop:hidden flex flex-col justify-center items-center">
        <div class="text-[21px] font-[700] mb-[14px]">WE ARE BREW MEMORIES!</div>
        <div class="text-[14px] font-[400] leading-[20px] mb-[2rem]">
          Welcome to Brooklyn’s best café in Park Slope, where passion meets perfection in every cup. Dive into a world
          of aromatic brews, handcrafted from globally sourced beans, and expertly roasted here in New York’s beloved
          borough.
        </div>
        <img class="mb-[3.5rem]" src="@/assets/img/about2.png" alt="">
        <div class="mb-[2.5rem]">
          We roast our coffee locally in small batches to ensure you get the freshest beans around. Not only is our
          coffee roasted to perfection, but all our drinks, including the finest bubble tea, as well as our meals and
          desserts, up hold the same standard of excellence!
        </div>
        <img class="mb-[3.5rem]" src="@/assets/img/about1.png" alt="">
        <div class="flex flex-col justify-center items-center mb-[3rem]">
          <div class="text-[21px] font-[700]">Freshly Made</div>
          <div class="text-center">Fresh coffee, quality drinks,<br> excellent meals!</div>
        </div>
        <img src="@/assets/img/about3.png" alt="">
      </div>
    </div>
    <div id="MENU" class="flex flex-col justify-center items-center bg-[#4B3426] py-[100px] relative">
      <div class="flex flex-col justify-center items-center">
        <div class="font-[300] text-white tablet:text-14px">our delicious offer</div>
        <div class="text-[1.5rem] text-white tablet:text-center tablet:mx-[10%]">Unique food and charming spot in
          Brooklyn!</div>
      </div>
      <div class="flex justify-center gap-[10%] w-full my-[2rem]">
        <div class="flex flex-col items-center justify-center w-[250px] tablet:hidden">
          <div v-for="(item, index) in menu1List" :key="index" class="w-full text-center">
            <div class="text-white py-[2rem]">{{ item }}</div>
            <div v-if="index !== menu1List.length - 1" class="w-full border-t border-dashed border-white" />
          </div>
        </div>
        <div class="flex flex-col items-center justify-center w-[250px] tablet:hidden">
          <div v-for="(item, index) in menu2List" :key="index" class="w-full text-center">
            <div class="text-white py-[2rem]">{{ item }}</div>
            <div v-if="index !== menu2List.length - 1" class="w-full border-t border-dashed border-white" />
          </div>
        </div>
        <div class="desktop:hidden">
          <div v-for="(item, index) in menu1List" :key="index" class="w-full text-center">
            <div class="text-white py-[2rem]">{{ item }}</div>
            <div class="w-full border-t border-dashed border-white" />
          </div>
          <div v-for="(item, index) in menu2List" :key="index" class="w-full text-center">
            <div class="text-white py-[2rem]">{{ item }}</div>
            <div v-if="index !== menu2List.length - 1" class="w-full border-t border-dashed border-white" />
          </div>
        </div>
      </div>
      <div class="bg-white py-[12px] px-[24px] rounded-full cursor-pointer" @click="goUrl()">Order Online</div>
      <img class="w-[450px] h-[320px] absolute top-[-25%] left-[20%] tablet:hidden" src="@/assets/img/menu.png" alt="">
      <div class="desktop:hidden absolute top-[-13%] left-0 flex">
        <img src="@/assets/img/menuP1.png" alt="">
        <img class="mb-[20%]" src="@/assets/img/menuP2.png" alt="">
      </div>
    </div>
    <!-- 六張圖區 -->
    <div
      class="w-full px-[61px] bg-white flex flex-wrap py-[157px] gap-x-[60px] gap-y-[28px] justify-center laptop:flex-nowrap laptop:flex-col tablet:flex-col tablet:flex-nowrap laptop:px-[48px] laptop:py-[36px] laptop:gap-x-0 laptop:gap-y-[26px] tablet:px-[48px] tablet:py-[36px] tablet:gap-x-0 tablet:gap-y-[26px]">
      <img v-for="p in 6" :src="getAssetsImgFile('m', `m${p}.png`)" alt=""
        class="object-cover w-1/4 h-1/2 laptop:w-full tablet:w-full">
    </div>
    <!-- 介紹 桌電板 -->
    <div class="flex gap-[113px] justify-center pb-[203px] pt-[60px] laptop:hidden tablet:hidden">
      <div class="flex flex-col gap-[72px]">
        <img class="w-[424px]" src="@/assets/img/c/c1.png" alt="coffee info">
        <span class="text-[32px] w-[466px]">Fresh coffee beans are used daily to provide a delicious cup of
          coffee.</span>
        <img class="w-[424px]" src="@/assets/img/c/c2.png" alt="coffee info">
      </div>
      <div class="flex flex-col gap-[72px] mt-[111px]">
        <span class="text-[32px] w-[466px]">A professional barista crafts a delicious cup of coffee just for you.</span>
        <img class="w-[424px]" src="@/assets/img/c/c3.png" alt="coffee info">
        <span class="text-[32px] w-[466px]">A refreshing cup of bubble tea is the perfect thirst quencher.</span>
      </div>
    </div>
    <!-- 介紹 手機板 -->
    <div
      class="flex flex-col gap-[46px] justify-center items-center px-[42px] pb-[174px] pt-[60px] desktop:hidden mac:hidden">
      <span class="text-[24px] w-full text-center !font-[400]">A professional barista crafts a delicious cup of coffee
        just for
        you.</span>
      <img class="w-full" src="@/assets/img/c/c1.png" alt="coffee info">
      <span class="text-[24px] w-full text-center !font-[400]">Fresh coffee beans are used daily to provide a delicious
        cup of
        coffee.</span>
      <img class="w-full" src="@/assets/img/c/c2.png" alt="coffee info">
      <span class="text-[24px] w-full text-center !font-[400]">A refreshing cup of bubble tea is the perfect thirst
        quencher.</span>
      <img class="w-full" src="@/assets/img/c/c3.png" alt="coffee info">
    </div>
    <!-- contact 桌電板 -->
    <img src="@/assets/img/c/contact.png" alt="contact" class="w-full object-contain laptop:hidden tablet:hidden">
    <!-- contact 手機版 -->
    <div class="relative desktop:hidden mac:hidden">
      <img src="@/assets/img/mo1.png" alt="contact" class="w-full object-contain">
      <img src="@/assets/img/mo2.png" alt="contact" class="object-contain absolute bottom-[-90px]">
    </div>
  </div>
  <div class="w-[53px] h-[53px] bg-[#D9D9D9] rounded-full fixed bottom-[24px] right-[20px] flex justify-center items-center">
    <img src="@/assets/icon/arrow.svg" alt="arrow" class="w-[40px] rotate-90" @click="goToTop()">
  </div>
</template>

<script setup lang="ts">
import { ref } from 'vue'
import { getAssetsImgFile } from '../utils/commonUse'
const content = ref(null)
const menu1List = ref<string[]>(['COFFEE', 'SPECIALTY LATTE', 'FRIZZY SPARKLING & SLUSH', 'FRESH FRUIT  TEA'])
const menu2List = ref<string[]>(['SPECIAL SMOOTHIE', 'LEMONADE', 'FOOD'])
const orderUrl = ref<string>('https://order.mealkeyway.com/customer/release/index?mid=45774946684268454942534476706e424837583342773d3d#/main')

const goUrl = (url?: string) => {
  if(!url){
    url = orderUrl.value
  }
  window.open(url, '_blank');
}

const goToTop = () => {
  window.scrollTo({
    top: 0,
    behavior: "smooth"
  })
}
</script>

<style lang="scss" scoped>
</style>