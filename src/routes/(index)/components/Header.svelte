<script>
  import Typewriter from "./Typewriter.svelte";
</script>

<header class="grid content-center justify-center grid-cols-1 md:grid-cols-2 md:grid-rows-1 min-h-screen md:min-h-fit">
  <div class="flex justify-center items-center flex-col px-2 h-full">
    <h1 class="text-s-primary text-8xl font-s-primary">Hello!</h1>
    <p class="text-white text-2xl my-4">
      I'm <span class="font-s-cursive">Mr-M1M3</span>
    </p>
    <p class="text-white">
      a <span class="text-s-primary font-bold text-2xl">
        <Typewriter type={["Web Developer", "Human Being"]} delay="300"/>
    </span>
    </p>
    <p class="text-s-primary font-s-primary text-5xl text-center hidden lg:block my-4">
      I Love to make the web look <span class="text-white block my-4 text-7xl">Cooler!!!</span>
    </p>
    <p class="hidden md:grid grid-cols-2 gap-3 my-4 w-2/3 justify-items-center items-center">
      <a href="/" class="btn primary w-1/2 md:w-full">Hire Me</a>
      <a href="/" class="btn secondary w-1/2 md:w-full">Resume</a>
    </p>
  </div>
  <div class="image-container grid md:flex justify-center items-center">
    <img src="/images/hero.svg" alt="" class="max-w-full md:w-full" data-aos="zoom-in"/>
    <p class="flex justify-center items-center px-2 md:hidden w-full">
      <a href="/" class="btn primary">Hire Me</a>
      <a href="/" class="btn secondary">Resume</a>
    </p>
  </div>
</header>

<style>
  .image-container{
    grid-template-columns: 1fr;
    grid-template-rows: 3fr 1fr;
    justify-items: center;
  }
  .btn{
    @apply border border-s-primary text-center rounded-md leading-10 px-4 py-1 w-full my-2 mx-2;
  }
  .btn.primary{
    @apply bg-s-primary font-bold;
  }
  .btn.secondary{
    @apply text-white font-s-secondary;
  }
</style>