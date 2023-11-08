<!-- <template>
  <div class="w-full fixed-navbar">
    <div class="mx-[2vw] 2xl:mx-[4vw]">
      <nav
        class="nav h-[70px] m-auto flex justify-between items-center"
        :class="{ active: isMobileMenuActive }"
      >
        <a href="/" class="text-4xl">&lt;Dev&gt;</a>
        <button @click="toggleMobileMenu" class="hamburger"></button>
        <ul class="flex text-2xl list-none gap-11 nav-list">
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
    background: #c940eb;
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

  /* Active Styles */

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
  <div class="fixed z-50 w-full navbar-container">
    <div class="mx-[2vw] 2xl:mx-[6vw]">
      <nav
        class="nav h-[70px] m-auto flex justify-between items-center"
        :class="{ active: isMobileMenuActive }"
      >
        <a href="/" class="text-4xl">&lt;dev&gt;</a>
        <button @click="toggleMobileMenu" class="hamburger"></button>
        <ul class="flex text-2xl list-none gap-11 nav-list">
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
  /* 0497d1 */
  background: linear-gradient(180deg, #141414 3rem, rgba(4, 151, 209, 0));
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

  /* Active Styles */

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
