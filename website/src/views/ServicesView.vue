<template>
    <div class="menu-item" @click="isOpen = !isOpen" >
        <a href ='#'>
            {{ title }}
        </a>
        <svg id="arrow" viewBox="0 0 1030 638" width="100">
            <path d="M1017 68L541 626q-11 12-26 12t-26-12L13 68Q-3 49 6 24.5T39 0h952q24 0 33 24.5t-7 43.5z" fill="#FFF"></path>
        </svg>
        <transition name="fade" apear>
         <div class="sub-menu" v-if="isOpen">
            <div class="menu-item">
              <router-link to="/about/Overview">Overview</router-link>
            </div>
            <div class="menu-item">
              <router-link to="/about/BO">Back Office</router-link>
            </div>
            <div class="menu-item">
              <router-link to="/about/PT">PainTrax</router-link>
            </div>
        </div>
        </transition>
    </div>
</template>

<script>
export default {
  name: 'services',
  props: ['title'],
  data () {
    return {
      isOpen: false,
      }
    }
}
</script>
<style>
.menu-item{
  margin-left: 20%;
  width: 100%;
  display: inline;
}
nav .menu-item svg {
    width: 10px;
    margin-left: 5px;
    margin-right: 20%;
}
nav .menu-item .sub-menu {
  z-index: 999;
  position: absolute;
  background-color: var(--dark-brown);
  top: calc(100% + 5px);
  left: 10%;
  transform: translateX(-50%);
  display: flex;
  flex-direction: column;
  width: 7rem;
  border-radius: 0px 0px 16px 16px;
}
.fade-enter-active,
.fade-leave-active {
  transition: all .5s ease-out;
}
.fade-enter,
.fade-leave-to {
  opacity: 0;
}
.sub-menu {
  cursor: pointer;
}
</style>