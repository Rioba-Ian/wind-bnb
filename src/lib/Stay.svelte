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

  import "iconify-icon";
</script>

<article>
  <img src={stay.photo} alt="stay.title" />

  <div class="my-4 flex justify-between">
    {#if stay.superHost}
      <span class="border-2 border-spacing-6 px-2 border-gray-500 rounded-md"
        >Super Host</span
      >
    {/if}
    <p class="text-gray-400 font-medium ml-auto">
      {stay.type}
      {#if stay.beds}
        <span>.</span>
        <span>{stay.beds} beds</span>
      {/if}
    </p>
    <p class="ml-4">
      <iconify-icon
        class="iconify inline-block bg-red-500"
        data-icon="mdi:star"
        data-inline="false"
      />
      {stay.rating}
    </p>
  </div>

  <h2 class="font-bold text-gray-600">{stay.title}</h2>
</article>
