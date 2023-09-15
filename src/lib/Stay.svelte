<script lang="ts">
  interface Stay {
    city: string;
    country: string;
    superHost: boolean;
    title: string;
    rating: number;
    maxGuests: number;
    type: string;
    beds: number | null;
    photo: string;
  }
  export let stay: Stay;

  import Icon from "@iconify/svelte";
</script>

<article>
  <img src={stay.photo} alt="stay.title" />

  <div class="my-2 flex items-center justify-start">
    {#if stay.superHost}
      <p class="mr-8">
        <span
          class="border-2 border-spacing-6 px-3 py-1 border-gray-500 rounded-xl"
          >Super Host</span
        >
      </p>
    {/if}
    <div class="flex items-center justify-between flex-grow" id="house-ratings">
      <p class="text-gray-400 flex items-center">
        <span>{stay.type}</span>
        {#if stay.beds}
          <span class="relative bottom-[0.25em] px-2 text-2xl font-bold">.</span
          >
          <span>{stay.beds} beds</span>
        {/if}
      </p>
      <p class="flex items-center ml-auto">
        <Icon icon="clarity:favorite-solid" color="#EB5757" class="mr-2" />
        {stay.rating}
      </p>
    </div>
  </div>

  <h2 class="font-bold text-neutral-800">{stay.title}</h2>
</article>
