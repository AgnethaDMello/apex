<template>
  <div>
    <transition-group name="fade" tag="div">
      <div id="gallery">
        <img :src="currentImg" />
      </div>
    </transition-group>
    <a class="prev" @click="prev" href="#">&#10094; </a>
    <a class="next" @click="next" href="#">&#10095; </a>
  </div>
</template>

<script>
import Globe from "../images/globe.png";
import Soil from "../images/soil.jpg";
import TechPeople from "../images/techpeople.jpg";
import GlobeEye from "../images/globeeye.jpg";
import WebCode from "../images/webcode.jpg";
import TouchSquare from "../images/touchsquare.jpg";
export default {
  name: "Slider",
  data() {
    return {
      images: [
        Globe,
        Soil,
        TechPeople,
        GlobeEye,
        WebCode,
        TouchSquare,
      ],
      timer: null,
      currentIndex: 0
    };
  },

  mounted: function() {
    this.startSlide();
  },

  methods: {
    startSlide: function() {
      this.timer = setInterval(this.next, 4000);
    },

    next: function() {
      this.currentIndex += 1;
    },
    prev: function() {
      this.currentIndex -= 1;
    }
  },

  computed: {
    currentImg: function() {
      return this.images[Math.abs(this.currentIndex) % this.images.length];
    }
  }
};
</script>

<style scoped>
.fade-enter-active,
.fade-leave-active {
  transition: all 0.9s ease;
  overflow: hidden;
  visibility: visible;
  position: absolute;
  width:100%;
  opacity: 1;
}

.fade-enter,
.fade-leave-to {
  visibility: hidden;
  width:100%;
  opacity: 0;
}

img {
  height:600px;
  width:85%;
  object-fit: cover;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

.prev, .next {
  cursor: pointer;
  position: absolute;
  top: 40%;
  width: auto;
  padding: 16px;
  color: white;
  font-weight: bold;
  font-size: 18px;
  transition: 0.7s ease;
  border-radius: 0 4px 4px 0;
  text-decoration: none;
  user-select: none;
}

.next {
  right: 0;
}

.prev {
  left: 0;
}

.prev:hover, .next:hover {
  background-color: rgba(0,0,0,0.9);
}

#gallery{
  background: var(--light-blue);
}
</style>