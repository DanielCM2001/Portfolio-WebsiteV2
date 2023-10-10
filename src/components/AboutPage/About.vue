<template>
  <div class="relative flex items-center justify-center">
    <img
      src="../../assets/img/DanielPhoto.png"
      alt=""
      class="absolute h-[350px] xs:h-[450px] rotate-90 transform -translate-y-1/4 top-[0%] z-0 md:translate-y-0 md:rotate-0 md:top-auto md:left-0 md:opacity-10 md:h-[600px] 2xl:h-[700px] 3xl:h-[800px] xl:opacity-100"
    />
    <div
      class="w-full xs:w-9/12 lg:w-full lg:mx-[20vw] xl:mx-[25vw] static-container mx-5 pt-[20vh] space-y-10"
    >
      <h1
        class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[40px]"
      >
        .about(Daniel)
      </h1>

      <p class="text-2xl">
        A front-end Web Developer passionate about creating interactive
        applications and experiences on the web.
      </p>

      <div class="flex flex-row space-x-5 text-lg sm:space-x-10">
        <button class="px-8 py-3 primaryButtons">Download</button>
        <button class="px-5 py-3 primaryButtons">xd</button>
        <button class="px-5 py-3 primaryButtons">xd</button>
      </div>

      <div class="flex flex-col space-y-5">
        <p class="text-2xl text-white">Main Skills</p>

        <ul
          class="grid gap-y-[1rem] md:grid-flow-col md:grid-cols-4 md:gap-x-[2rem]"
        >
          <li>Frontend, UX/UI</li>
          <li>JavaScript, CSS, HTML, Vue, React, Tailwind</li>
          <li>SQL, Solidity, Ethers.js, Cloud Computing, C#</li>
          <li>Figma, Adobe XD</li>
        </ul>
      </div>

      <div class="flex flex-col space-y-5">
        <p class="text-2xl text-white">Experience</p>

        <ul
          class="grid gap-y-[1rem] md:grid-flow-col md:grid-cols-4 md:gap-x-[2rem]"
        >
          <li>
            <p
              class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px]"
            >
              Web Developer
            </p>
            <p class="text-[18px]">@Risidio</p>
            <p class="text-[15px]">2023-2023</p>
          </li>
          <li>
            <p
              class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px]"
            >
              Cloud Consultant
            </p>
            <p class="text-[18px]">@Accenture</p>
            <p class="text-[15px]">2021-2021</p>
          </li>
          <li>
            <p
              class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px]"
            >
              Web Developer
            </p>
            <p class="text-[18px]">@Sermocol</p>
            <p class="text-[15px]">2021-2021</p>
          </li>
          <li>
            <p
              class="text-[#c940eb] [text-shadow:0_4px_50px_rgba(201,64,235,1)] text-[20px]"
            >
              .NET Developer
            </p>
            <p class="text-[18px]">@Sermocol</p>
            <p class="text-[15px]">2021-2021</p>
          </li>
        </ul>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {};
  },
};
</script>

<style scoped>
.primaryButtons {
  border-radius: 20px;
  background: #c940eb;
  box-shadow:
    0px 5px 5px 0px #8c5dc9 inset,
    0px 4px 50px 0px #c940eb;
}

.static-container {
  min-height: 100vh;
  perspective: 900px;
  perspective-origin: 50% 50vh;
}
</style>
