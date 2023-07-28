<script>
  import Magnify from "svelte-material-icons/Magnify.svelte";
  let windBnbLogo = "/logo.svg";
</script>

<nav class="py-6">
  <div class="navbar flex items-center justify-between">
    <img src={windBnbLogo} width="120" height="100" alt="windbnb logo" />

    <form id="search-results" class="flex items-center">
      <input
        placeholder="Helsinki, Finland"
        class="shadow appearance-none border rounded w-2/3 py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
        name="location"
        id="location"
      />
      <input
        placeholder="Add guests"
        class="shadow appearance-none border rounded w-2/3 py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
        name="location"
        id="location"
      />
      <label for="location" class="py-2 px-3 outline-4 cursor-pointer"
        ><Magnify size={32} color="red" /></label
      >
    </form>
  </div>
</nav>

<style>
  #search-results {
    /* outline: 2px solid pink; */
  }
</style>
