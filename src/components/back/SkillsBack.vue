<template>
  <div class="flex flex-row items-stretch w-full pt-10">
    <div class="items-center justify-center hidden xs:flex xs:w-3/12">
      <div class="items-stretch w-5 h-full separatorBar"></div>
    </div>
    <div class="w-full xs:w-9/12">
      <h1 class="text-4xl">What I'm really good at</h1>

      <div
        class="bg-gray-800 flex flex-col items-center justify-center py-10 space-y-10 md:justify-start md:flex-row md:space-y-0 md:space-x-5"
      >
        <!-- Box -->
        <div
          class="box flex flex-col mx-5 md:mx-0 md:w-[120px] md:h-[120px] lg:w-[160px] lg:h-[160px]"
          v-for="(item, index) in skillItems"
          :key="index"
        >
          <!-- Content inside of the box -->
          <div
            class="flex flex-row items-stretch justify-center px-10 py-6 space-x-5 md:space-x-0 md:flex-col md:items-center md:px-8 md:py-8"
          >
            <div class="flex w-1/5 md:w-full md:items-center md:justify-center">
              <div
                class="item-container md:w-[50px] md:h-[50px] lg:w-[80px] lg:h-[80px]"
              >
                <img :src="item.src" class="object-contain w-full h-full" />
              </div>
            </div>
            <div
              class="flex items-center justify-start w-4/5 md:w-full md:justify-center"
            >
              <h1 class="text-xl">{{ item.title }}</h1>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      skillItems: [
        {
          src: new URL(`@/assets/img/VueIcon.png`, import.meta.url),
          title: "Vue.JS",
        },
        {
          src: new URL(`@/assets/img/ReactIcon.png`, import.meta.url),
          title: "React",
        },
        {
          src: new URL(`@/assets/img/ReactIcon.png`, import.meta.url),
          title: "Design",
        },
        {
          src: new URL(`@/assets/img/OtherIcon.png`, import.meta.url),
          title: "Other",
        },
      ],
    };
  },
};
</script>

<style scoped>
.box {
  border-radius: 40px;
  background: #151417;
  box-shadow:
    0px 3px 3px 0px #8c5dc9 inset,
    0px 4px 40px 0px #c940eb;
}

.separatorBar {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}
</style>

<!--  <template>
    <div class="flex flex-row items-stretch w-full">
      <div
        class="items-center justify-center hidden xs:flex xs:w-3/12 md:w-2/5 lg:w-4/11 bg-slate-700"
      >
        <div class="items-stretch w-5 h-full separatorBar"></div>
      </div>
      <div class="w-full xs:w-9/12 md:w-3/5 lg:w-8/11 bg-slate-800">
        <h1 class="text-4xl">What I'm really good at</h1>
  
        <div
          class="flex flex-col items-center justify-center py-10 space-y-10 lg:justify-start lg:flex-row lg:space-y-0 lg:space-x-10"
        >
          <div
            v-for="(item, index) in skillItems"
            :key="index"
            class="box w-[200px] h-[200px] lg:w-[140px] lg:h-[140px] xl:w-[160px] xl:h-[160px]"
          >
            <div class="flex flex-col items-center justify-center px-8 py-8">
              <div
                class="item-container w-[120px] h-[120px] lg:w-[50px] lg:h-[50px] xl:w-[80px] xl:h-[80px]"
              >
                <img :src="item.src" class="object-contain w-full h-full" />
              </div>
              <h1 class="text-xl">{{ item.title }}</h1>
            </div>
          </div>
        </div>
      </div>
    </div>
  </template>
  
  
  Add when connecting the bars the following:
    
        box-shadow:
      0px -5px 5px 0px #8c5dc9 inset,
      0px 4px 50px 0px #c940eb;
      
      and -my margin on the div itself
  
  
  
  
  -->
