<script lang="ts">
  import Magnify from "svelte-material-icons/Magnify.svelte";
  let windBnbLogo = "/logo.svg";

  import Modal from "./Modal.svelte";
  let isModalOpen = false;

  const openModal = () => {
    isModalOpen = true;
  };

  const closeModal = () => {
    isModalOpen = false;
  };
</script>

<nav class="py-6 relative">
  <div class="navbar flex items-center justify-between">
    <img src={windBnbLogo} width="120" height="100" alt="windbnb logo" />

    <form id="search-results" class="flex items-center">
      <input
        placeholder="Helsinki, Finland"
        class="shadow appearance-none border rounded w-2/3 py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
        name="location"
        id="location"
        on:click={openModal}
      />
      <input
        placeholder="Add guests"
        class="shadow appearance-none border rounded w-2/3 py-2 px-3 text-gray-700 leading-tight focus:outline-none focus:shadow-outline"
        type="text"
        name="location"
        id="location"
        on:click={openModal}
      />
      <label for="location" class="py-2 px-3 outline-4 cursor-pointer"
        ><Magnify size={32} color="red" /></label
      >
    </form>
  </div>

  <Modal isOpen={isModalOpen} close={closeModal} />
</nav>

<style>
  #search-results {
    /* outline: 2px solid pink; */
  }
</style>
