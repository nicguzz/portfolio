<template>
  <div class="skills">
    <a id="skills">
      <h1>Skills</h1>
    </a>

    <div class="card-container">
      <div class="card" @mouseover="htmlSkill" @mouseout="htmlSkill">
        <img
          id="html-image"
          title="HTML"
          class="card-image"
          src="https://cdn-icons-png.flaticon.com/512/3128/3128323.png"
          alt=""
        />
        <div class="skills-desc" v-if="html_boolean">
          <p>HTML</p>
        </div>
      </div>
      <div class="card" @mouseover="cssSkill" @mouseout="cssSkill">
        <img
          id="css-image"
          class="card-image"
          src="https://cdn-icons-png.flaticon.com/512/732/732190.png"
          alt=""
        />
        <div class="skills-desc" v-if="css_boolean">
          <p>CSS</p>
        </div>
      </div>
      <div class="card" @mouseover="jsSkill" @mouseout="jsSkill">
        <img
          title="Javascript"
          id="javascript"
          class="card-image"
          src="https://cdn-icons-png.flaticon.com/512/5968/5968292.png"
          alt=""
        />
        <div class="skills-desc" v-if="js_boolean">
          <p>JavaScript</p>
        </div>
      </div>
      <div class="card" @mouseover="vueSkill" @mouseout="vueSkill">
        <img
          id="vuejs"
          title="VueJS"
          class="card-image"
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/9/95/Vue.js_Logo_2.svg/1184px-Vue.js_Logo_2.svg.png"
          alt=""
        />
        <div class="skills-desc" v-if="vue_boolean">
          <p>VueJS</p>
        </div>
      </div>
      <div class="card" @mouseover="sbSkill" @mouseout="sbSkill">
        <img
          title="Supabase"
          class="card-image"
          src="https://seeklogo.com/images/S/supabase-logo-DCC676FFE2-seeklogo.com.png"
          alt=""
        />
        <div class="skills-desc" v-if="sb_boolean">
          <p>Supabase</p>
        </div>
      </div>
      <div class="card" @mouseover="pySkill" @mouseout="pySkill">
        <img
          title="Python"
          class="card-image"
          src="https://upload.wikimedia.org/wikipedia/commons/thumb/c/c3/Python-logo-notext.svg/1869px-Python-logo-notext.svg.png"
          alt=""
        />
        <div class="skills-desc" v-if="py_boolean">
          <p>Python</p>
        </div>
      </div>
      <div class="card" @mouseover="gitSkill" @mouseout="gitSkill">
        <img
          title="Git"
          class="card-image"
          src="https://git-scm.com/images/logos/downloads/Git-Icon-1788C.png"
          alt=""
        />
        <div class="skills-desc" v-if="git_boolean">
          <p>Git</p>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
import { ref } from "vue";

let html_boolean = ref(false);
let css_boolean = ref(false);
let js_boolean = ref(false);
let vue_boolean = ref(false);
let sb_boolean = ref(false);
let py_boolean = ref(false);
let git_boolean = ref(false);

function htmlSkill() {
  html_boolean.value = !html_boolean.value;
  return html_boolean.value;
}

function cssSkill() {
  css_boolean.value = !css_boolean.value;
  return css_boolean.value;
}

function jsSkill() {
  js_boolean.value = !js_boolean.value;
  return js_boolean.value;
}

function vueSkill() {
  vue_boolean.value = !vue_boolean.value;
  return vue_boolean.value;
}

function sbSkill() {
  sb_boolean.value = !sb_boolean.value;
  return sb_boolean.value;
}
function pySkill() {
  py_boolean.value = !py_boolean.value;
  return py_boolean.value;
}

function gitSkill() {
  git_boolean.value = !git_boolean.value;
  return git_boolean.value;
}

function scrollToTop() {
  let currentScroll = document.documentElement.scrollTop,
    int = setInterval(frame, 3);

  function frame() {
    if (0 > currentScroll) clearInterval(int);
    else {
      currentScroll = currentScroll - 12;
      document.documentElement.scrollTop = currentScroll;
    }
  }
}
</script>

<style></style>
