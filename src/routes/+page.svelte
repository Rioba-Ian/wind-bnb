<script>
  import Navbar from "$lib/Navbar.svelte";
  import Stay from "$lib/Stay.svelte";
  import staysData from "../stays.json";

  export let stays = staysData;
</script>

<div id="app-container">
  <Navbar />
  <main class="py-8">
    <div id="title" class="flex items-center justify-between">
      <h1 class="text-neutral-800 text-3xl font-bold">Stays in Finland</h1>
      <p class="text-zinc-800">{stays.length}+stays</p>
    </div>
    <div id="content" class="py-5">
      <section
        id="stays-grid"
        class="grid grid-col-1 grid-cols-3 gap-x-8 gapy-6 grid-flow-row-dense"
      >
        {#each stays as stay}
          <div class="py-5">
            <Stay {stay} />
          </div>
        {/each}
      </section>
    </div>
  </main>
</div>

<style>
  #app-container {
    width: min(80%, 1440px);
    margin: 0 auto;
  }

  #stays-grid {
    grid-auto-rows: auto;
  }

  #stays-grid > div:nth-child(1) {
    grid-column: span 1;
  }

  #stays-grid > div:nth-child(2) {
    grid-column: span 2;
  }

  #stays-grid > div:nth-child(2) {
    grid-row: span 2;
  }

  #stays-grid > div:nth-child(4) {
    grid-row: span 2;
  }

  #stays-grid > div:nth-child(10) {
    grid-column: 1/ 2;
  }
</style>
