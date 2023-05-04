<div class="flex flex-row my-4 mx-12 justify-around">
  <div class="container max-w-md">

		<div id="Sign" class="">
			<div
				class="text-6xl lg:text-8xl font-bold text-success-500 bungee emdash text-center max-w-sm mt-2 flicker-btn"
			>
				Design <br /> as a <br /> Service
			</div>
			<div class="max-w-md text-xl lg:text-3xl font-thin text-center">
				Pay-as-you go design subscriptions <br /> for websites & apps.
			</div>
		</div>
		<div class="container flex flex-row justify-center lg:justify-end max-w-md">
			<a
				class="btn mt-12 border-b-4 border-primary-700 variant-filled-primary font-black rounded-none"
				href="#meow"
			>
				Compare Plans
			</a>
		</div>
  </div>
  <img src="logos/hero.svg" alt="" class="hidden md:block md:h-[350px] lg:block lg:h-[450px]">
</div>



<style>
	#Sign {
		/* transform it 20 deg */
		transform: rotate(-5deg);
	}

@keyframes flicker {
  5%, 6%, 7%, 8% {
    opacity: 0.9;
  }
  90% {
    opacity: 1;
  }
  96%, 98%, 99% {
    opacity: 0.7;
  }
  100% {
    opacity: 1;
  }
}

.flicker-btn {
  animation: flicker .2s infinite;
}

</style>
