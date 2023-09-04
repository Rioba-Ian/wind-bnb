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
</script>

<article>
  <img src={stay.photo} alt="stay.title" />

  <div>
    {#if stay.superHost}
      <span>Super Host</span>
    {/if}
    <p>{stay.type} . {stay.beds} beds</p>
    <p>{stay.rating}</p>
  </div>

  <h2>{stay.title}</h2>
</article>
