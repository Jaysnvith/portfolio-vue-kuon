<template>
    <div class="flex flex-col gap-[2.5rem]">
      <div class="divCenter">
        <p
          id="artworks_intro"
          ref="artworksIntro"
          class="lg:text-xl text-md acrlyic w-auto text-center selector"
        ></p>
      </div>
      <section class="pt-2">
        <h2 class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2">
          Images
        </h2>
        <br /> <br />
        <img class="shadow-xl bg-auto bg-center rounded-md border-10 min-w-32" src="/assets/images/Berserk.png" alt="Berserk">
        <br /> <br />
        <img class="shadow-xl bg-auto bg-center rounded-md border-10 min-w-32" src="/assets/images/Ozymandias.png" alt="Ozymandias">
        <br /> <br />
        <img class="shadow-xl bg-auto bg-center rounded-md border-10 min-w-32" src="/assets/images/SilentHill.png" alt="Silent Hill">
        <br /> <br />
      </section>
      <section class="pt-2">
        <h2 class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2">
          Videos
        </h2>
        <br /> <br />
        <video class="shadow-xl bg-auto bg-center rounded-md border-10 min-w-32" controls>
          <source src="/assets/images/KillthePast.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </section>
    </div>
  </template>
  
  <script>
  import TypeIt from 'typeit';
  import 'animate.css';
  import { ref } from 'vue';
  
  export default {
      data() {
          return {
              display: false,
          };
      },
      setup() {
          const artworksIntro = ref('');
  
          if (artworksIntro.value !== '') {
              artworksIntro.value === '';
          }
      },
      mounted() {
          new TypeIt('#artworks_intro', {
              speed: 50,
              waitUntilVisible: true,
              startDelay: 2000,
              startDelete: true,
              // remove cursor when finished
              afterComplete: function (instance) {
                  instance.destroy();
              },
          })
              .type('This is my art !')
              .go();
      },
  };
  </script>
  
  <style>
  .selector {
    background-color: var(--bg-sel);
  }
  
  .copyright {
    animation: fadeInLeft; /* referring directly to the animation's @keyframe declaration */
    animation-duration: 1s; /* don't forget to set a duration! */
    animation-delay: 3s;
  }
  
  /* @keyframes copyright {
    0% {
      opacity: 0;
    }
    100% {
      opacity: 1;
      visibility: visible;
    }
  } */
  </style>