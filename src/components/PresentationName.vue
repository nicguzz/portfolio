<template>
  <div
    :class="[
      aboutBoolean
        ? 'photo-about animate__animated animate__bounceInLeft'
        : 'photo-area',
      errorClass,
    ]"
  >
    <img
      class="photo-url"
      src="https://res.cloudinary.com/dbmzbapuj/image/upload/v1679044068/nicdev_jeoqtr.jpg"
      alt="Photo"
    />
    <div class="intro-name">
      <h1 class="animate__animated animate__pulse">Nicolás Guzzetti</h1>
      <h2 class="animate__animated animate__fadeInUpBig font-normal">
        Frontend Developer
      </h2>
    </div>

    <div
      class="aboutme-container animate__animated animate__slideInUp"
      v-if="aboutBoolean"
    >
      <p class="aboutme-text">
        Hi!👋 Welcome to my portfolio!
        <br />
        I am Nic!
        <br />
        From Cascais, 🇵🇹 & in Barcelona🇪🇸 since 2016, I recently decided to get
        into tech world, getting interested in web development.
        <br />
        Below you will find some projects that I have done.
        <br />
        Enjoy!
      </p>
    </div>
  </div>
  <div class="aboutme">
    <button class="click-button" @click="aboutMe">About me</button>
    <a
      target="__blank"
      href="https://mega.nz/file/FUsz2T5K#PX9mdRtMBtUq2Fg_FVoiYs1UtGreHMs46Yu5lC3CjiA"
    >
      <button class="click-button">Download CV</button>
    </a>
  </div>
</template>

<script setup>
import "animate.css";
import { ref } from "vue";

let aboutBoolean = ref(false);

function aboutMe() {
  aboutBoolean.value = !aboutBoolean.value;
  return aboutBoolean;
}
</script>

<style></style>
