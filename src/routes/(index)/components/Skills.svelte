<script>
  import { browser } from "$app/environment";
  import Icon from "@iconify/svelte";
  export let data = [];
  data = data.sort((a, b) => a.order - b.order);
</script>
<section class="skills px-5 py-3 grid grid-cols-1 md:grid-cols-2 my-3 overflow-hidden">
  <div class="coding flex justify-center items-center">
    <img src="/images/coding.svg" alt="" class="max-w-md" data-aos="fade-right"/>
  </div>
  <div class="heading-with-skills flex flex-col">
    <h1 class="heading" id="skills">Things I work with</h1>
    <div class="skills-container flex-grow flex content-center flex-wrap justify-center items-center ">
      {#if browser}
        {#each data as datum (datum.id)}
          <div class="skill flex justify-center items-center flex-col mx-2 my-3 md:p-3" data-aos="fade-left">
            <p class="text-6xl">
              <Icon icon={datum.iconify_class} />
            </p>
            <p class="text-md text-white font-bold my-1 font-s-secondary">{datum.name}</p>
          </div>
        {/each}
      {/if}
    </div>
  </div>
</section>