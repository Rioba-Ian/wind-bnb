<script lang="ts">
  export let isOpen = false;

  export let close = () => {};
</script>

{#if isOpen}
  <div class="modal absolute bg-white w-full">
    <div class="modal-content">
      <span
        class="close text-3xl ml-auto"
        aria-roledescription="close modal"
        on:click={close}>&times;</span
      >

      <!-- add search functionality here -->
      <div class="">
        <form action="" class="flex items-center justify-between">
          <div class="relative z-0 w-1/3">
            <input
              type="text"
              id="floating_standard"
              class="block py-2 px-1 w-full text-gray-900 bg-transparent focus-within:border-2 border-gray-300 rounded-xl appearance-none focus:outline-none focus:ring-0 peer"
              placeholder=" "
            />
            <label
              for="floating_standard"
              class="absolute px-2 text-gray-500 dark:text-gray-800 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-focus:text-gray-900 peer-placeholder-shown:scale-300 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-8"
              >LOCATION</label
            >
          </div>

          <div class="relative z-0 w-1/3">
            <input
              type="text"
              id="floating_standard"
              class="block py-2.5 px-1 w-full text-sm text-gray-900 bg-transparent border-0 focus-within:border-2 border-gray-300 rounded-xl appearance-none focus:outline-none focus:ring-0 peer"
              placeholder=" "
            />
            <label
              for="floating_standard"
              class="absolute px-2 text-gray-500 dark:text-gray-800 duration-300 transform -translate-y-6 scale-75 top-3 -z-10 origin-[0] peer-focus:left-0 peer-focus:text-gray-900 peer-placeholder-shown:scale-300 peer-focus:outline-2 peer-placeholder-shown:translate-y-0 peer-focus:scale-75 peer-focus:-translate-y-8"
              >GUESTS</label
            >
          </div>

          <div
            class="w-1/3 flex items-center justify-center outline-black outline-1"
          >
            <button
              type="submit"
              class="inline-flex items-center py-2.5 px-3 ml-2 text-sm font-medium text-white bg-[#EB5757] rounded-lg border border-[#EB5757] hover:bg-[#EB5757] focus:ring-4 focus:outline-none focus:ring-[#EB5757]"
            >
              <svg
                class="w-4 h-4 mr-2"
                aria-hidden="true"
                xmlns="http://www.w3.org/2000/svg"
                fill="none"
                viewBox="0 0 20 20"
              >
                <path
                  stroke="currentColor"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                  stroke-width="2"
                  d="m19 19-4-4m0-7A7 7 0 1 1 1 8a7 7 0 0 1 14 0Z"
                />
              </svg>Search
            </button>
          </div>
        </form>
      </div>
    </div>
  </div>
{/if}

<style>
  /* style for seach modal */
</style>
