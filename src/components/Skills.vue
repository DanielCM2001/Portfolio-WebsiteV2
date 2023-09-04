<template>
  <div class="min-h-screen flex justify-center items-center">
    <div class="flex justify-center items-center w-full flex-col md:flex-row">
      <div class="w-full flex justify-center items-center">
        <!--  <div class="box">1</div>
        <div class="box">2</div>
        <div class="box">3</div>
        <div class="box">4</div> -->

        <div
          class="mx-4 my-4 flex flex-col space-y-20 lg:flex-row lg:space-x-20"
        >
          <div class="box"></div>
          <div class="box"></div>
          <div class="box"></div>
          <div class="box"></div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  setup() {
    return {};
  },
};
</script>

<style scoped>
.box {
  width: 253px;
  height: 230px;
  border-radius: 40px;
  background: #313339;
  box-shadow: 0px 5px 5px 0px #8c5dc9 inset, 0px 4px 40px 0px #c940eb;
}
</style>
