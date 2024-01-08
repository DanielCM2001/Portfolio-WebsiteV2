<template>
  <div
    class="fixed z-50 w-full text-[1.1rem] text-[#cbc8c4] navbar-container secondaryFont"
  >
    <!--  2xl:mx-[6vw] -->
    <!-- hideNavBar -->
    <div class="mx-[1.25rem] py-[.75rem]">
      <nav
        class="nav h-[40px] m-auto flex justify-between items-center"
        :class="{ active: isMobileMenuActive }"
      >
        <div class="flex flex-row">
          <!-- <a href="/" class="">Daniel Martins</a> -->
          <a
            href="/"
            class="text-[25px] font-extrabold text-[#d8d4cf] tracking-tight mt-1"
            >daniel</a
          >
        </div>

        <button @click="toggleMobileMenu" class="hamburger"></button>
        <ul class="flex list-none gap-7 nav-list items-center">
          <li><a href="#">about</a></li>
          <li><a href="#">services</a></li>
          <li><a href="#">projects</a></li>
          <!--  <li><a href="#">contact</a></li> -->

          <!-- bg-[#C7C8BF] text-[#131313] -->
          <!-- border border-[#cbc8c4] -->
          <a
            class="relative py-[.40rem] px-[2rem] rounded-[2rem] bg-[#C7C8BF] text-[#131313]"
            href="#contact"
            ><span class="relative w-fit"
              ><span class="absolute"></span><span>contact</span></span
            ></a
          >
        </ul>
      </nav>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      isMobileMenuActive: false,
    };
  },
  methods: {
    toggleMobileMenu() {
      this.isMobileMenuActive = !this.isMobileMenuActive;
    },
  },
};
</script>

<style scoped>
.navbar-container {
  /* background: linear-gradient(180deg, #0f0e0f 3rem, rgba(4, 151, 209, 0)); */

  background: transparent;

  /* background-color: #0497d1; */
  /* background: #131313;
  border-bottom: 1px solid; */

  /*  background-color: transparent;
  backdrop-filter: blur(2px); */
}

.navbar-container-sky {
  background: linear-gradient(180deg, #0497d1 3rem, rgba(4, 151, 209, 0));
  color: #ffffff;
  /*  background-color: transparent;
  backdrop-filter: blur(2px); */
}
.hamburger {
  display: none;
  border: none;
  background: none;
  border-top: 3px solid #fff;
  cursor: pointer;
}

.hamburger::after,
.hamburger::before {
  content: " ";
  display: block;
  width: 30px;
  height: 3px;
  background: #fff;
  margin-top: 5px;
  position: relative;
  transition: 0.3s;
}

@media (max-width: 750px) {
  .hamburger {
    display: block;
    z-index: 41;
  }

  .nav-list {
    position: fixed;
    top: 0;
    left: 0;
    width: 100vw;
    height: 100vh;
    background: #131313;
    clip-path: circle(100px at 90% -15%);
    transition: 1s ease-out;

    flex-direction: column;
    justify-content: space-around;
    align-items: center;
    gap: 0;

    pointer-events: none;
    z-index: 40;
  }

  .nav-list a {
    opacity: 0;
  }

  .nav-list li:nth-child(1) a {
    transition: 0.5s 0.2s;
  }

  .nav-list li:nth-child(2) a {
    transition: 0.5s 0.4s;
  }

  .nav-list li:nth-child(3) a {
    transition: 0.5s 0.6s;
  }

  .nav.active .nav-list {
    clip-path: circle(1500px at 90% -15%);
    pointer-events: all;
  }

  .nav.active .nav-list a {
    opacity: 1;
  }

  .nav.active .hamburger {
    position: fixed;
    top: 26px;
    right: 16px;
    border-top-color: transparent;
  }

  .nav.active .hamburger::before {
    transform: rotate(135deg);
  }

  .nav.active .hamburger::after {
    transform: rotate(-135deg);
    top: -7px;
  }
}
</style>
