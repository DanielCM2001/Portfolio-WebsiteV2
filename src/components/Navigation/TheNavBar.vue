<!-- <template>
  <div class="fixed z-50 w-full text-[24px] 3xl:text-[1.3vw] navbar-container">
    <div class="mx-[2vw] 2xl:mx-[6vw]">
      <nav
        class="nav h-[70px] m-auto flex justify-between items-center"
        :class="{ active: isMobileMenuActive }"
      >
        <a href="/">&lt;dev&gt;</a>
        <button @click="toggleMobileMenu" class="hamburger"></button>
        <ul class="flex list-none gap-11 nav-list">
          <li>
            <router-link to="/" @click="toggleMobileMenu"
              >.daniel()</router-link
            >
          </li>
          <li>
            <router-link to="/about" @click="toggleMobileMenu"
              >.about()</router-link
            >
          </li>
          <li><a href="#">.email()</a></li>
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
  background: linear-gradient(180deg, #131313 3rem, rgba(4, 151, 209, 0));
}

.navbar-container-sky {
  background: linear-gradient(180deg, #0497d1 3rem, rgba(4, 151, 209, 0));
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
    background: #c3023a;
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
 -->

<template>
  <div
    class="fixed z-50 w-full text-[24px] 3xl:text-[1.4vw] text-[#F5EEE6] navbar-container "
  >
    <!--  2xl:mx-[6vw] -->
    <!-- hideNavBar -->
    <div class="mx-[4vw] 2xl:mx-[4vw] ">
      <nav
        class="nav h-[80px] m-auto flex justify-between items-center"
        :class="{ active: isMobileMenuActive }"
      >
        <div class="text-[18px] 3xl:text-[0.8vw] space-x-10 flex flex-row">
          <a href="/" class="secondaryFont">Daniel Martins</a>
          <!-- Change the fonts -->
          <a href="/" class="hidden lg:block secondaryFont"
            >DEVELOPER, UX/UI DESIGNER</a
          >
        </div>

        <button @click="toggleMobileMenu" class="hamburger"></button>
        <ul class="flex list-none gap-14 nav-list">
          <li>
            <router-link to="/about" @click="toggleMobileMenu"
              >.about()</router-link
            >
          </li>
          <li><a href="#">.email()</a></li>
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
  background: linear-gradient(180deg, #131313 3rem, rgba(4, 151, 209, 0)); 
  /*  background-color: transparent;
  backdrop-filter: blur(2px); */
}

.navbar-container-sky {

  background: linear-gradient(180deg, #0497d1 3rem, rgba(4, 151, 209, 0)); 
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
    background: #c3023a;
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
