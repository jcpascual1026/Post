<script lang="ts">
  let search = "";
</script>

<div class="px-12 py-7">
  <section class="text-center my-10">
    <h1 class="text-5xl font-bold font-poppins">Freedom Post</h1>
  </section>

  <section class="flex flex-col md:flex-row items-center justify-center gap-4 px-4 mb-6 font-poppins">
    <div class="flex flex-wrap gap-2 justify-center md:justify-start">
      <button class="uppercase text-green-500 border border-green-500 bg-white font-bold shadow-md rounded-xl px-5 py-2 text-xs active:shadow-none active:translate-x-[3px] active:translate-y-[3px] cursor-pointer">
        Approve
      </button>
      <button class="uppercase text-red-600 border border-red-600 bg-white font-bold shadow-md rounded-xl px-5 py-2 text-xs active:shadow-none active:translate-x-[3px] active:translate-y-[3px] cursor-pointer">
        Decline
      </button>
      <button class="uppercase text-gray-700 border border-gray-700 bg-white font-bold shadow-md rounded-xl px-5 py-2 text-xs active:shadow-none active:translate-x-[3px] active:translate-y-[3px] cursor-pointer">
        Cancel
      </button>
    </div>

    <div class="flex items-center gap-2 border border-black rounded-xl px-3 py-2 ml-0 md:ml-10 w-full max-w-md">
      <input bind:value={search} type="text" placeholder="Search for any post..." class="w-full bg-transparent border-none text-sm font-poppins focus:outline-none focus:ring-0"/>
    <!-- svelte-ignore a11y_label_has_associated_control -->
      <label>
        <i class="fa-solid fa-magnifying-glass text-white bg-neutral-800 p-2 rounded-xl"></i>
      </label>
    </div>
  </section>

  <section class="text-center my-6 font-poppins">
    <div class="flex flex-wrap justify-center gap-3">
      {#each ["All", "General", "Crushes", "Tech Idea", "Shoutout", "Question", "Event Suggestions", "Rants"] as tag}
        <button class="text-xs text-white uppercase bg-neutral-900 shadow-md rounded-xl px-5 py-2 border border-black active:shadow-none active:translate-x-[3px] active:translate-y-[3px] cursor-pointer">
        {tag}
        </button>
      {/each}
    </div>
  </section>
</div>