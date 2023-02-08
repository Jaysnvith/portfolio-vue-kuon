<template>
  <div class="flex flex-col gap-[2.5rem]">
    <!-- introduction section -->
    <div class="divCenter">
      <p
        id="landing_intro"
        ref="landingIntro"
        class="lg:text-xl text-md acrlyic w-auto text-center selector"
      ></p>
    </div>
    <section class="">
      <h1 class="text-4xl font-bold">Panji Maulana Buckriawan</h1>
      <h3 class="text-lg">System Information Fresh Graduate</h3>
    </section>
    <section class="pt-2">
      <h2 class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2">
        About Me
      </h2>
      <br />
      <p class="lg:text-lg text-sm text-justify leading-6">
        &nbsp;&nbsp;&nbsp;&nbsp; My name is Panji Maulana Buckriawan, 
        I’m a 22 years old male and a fresh graduate with bachelors degree in information systems who is familiar with system development and graphic design. 
        I’m a creative and an organized person who likes to get job done efficiently and in best way possible, 
        good at analysis and able to work and communicate well with a team on a project.
      </p>
      <br />
    </section>
    <section>
      <h2 class="lg:text-2xl text-lg font-bold underline underline-offset-8 decoration-2">
        My Contact
      </h2>
      <br />
      <ul>
        <li class="list-disc transition ease-in-out delay-150 hover:-translate-y-1 hover:scale-10 duration-300">
          <a href="https://twitter.com/buckriawan" class="font-medium text-blue-600 dark:text-blue-500">Twitter</a>
        </li>
        <li class="list-disc transition ease-in-out delay-150 hover:-translate-y-1 hover:scale-10 duration-300">
          <a href="https://www.instagram.com/buckriawan/" class="font-medium text-blue-600 dark:text-blue-500">Instagram</a>
        </li>
        <li class="list-disc transition ease-in-out delay-150 hover:-translate-y-1 hover:scale-10 duration-300">
          <a href="https://www.linkedin.com/in/panjimb/" class="font-medium text-blue-600 dark:text-blue-500">Linkdn</a>
        </li>
        <li class="font-medium text-blue-600 dark:text-blue-500 list-disc transition ease-in-out delay-150 hover:-translate-y-1 hover:scale-10 duration-300">
          panjim0b@gmail.com
        </li>
      </ul>
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
		const landingIntro = ref('');

		if (landingIntro.value !== '') {
			landingIntro.value === '';
		}
	},
	mounted() {
		new TypeIt('#landing_intro', {
			speed: 50,
			waitUntilVisible: true,
			startDelay: 2000,
			startDelete: true,
			// remove cursor when finished
			afterComplete: function (instance) {
				instance.destroy();
			},
		})
			.type('Welcome stranger, take a look around !')
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
