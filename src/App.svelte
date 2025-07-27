<script lang="ts">
  import BusinessCard from "./components/BusinessCard.svelte";
  import ProjectCards from './components/ProjectCards.svelte';
</script>

<!-- <Navbar /> -->
<main>
  <!-- ########## Hero section ########## -->
  <section class="max-w-screen-xl mx-auto px-5 flex flex-col justify-center items-center py-5 md:py-10 lg:py-20">
    <BusinessCard />
  </section>
  <!-- ########## My Work Section ########## -->
  <div class="bg-[#333]/5  rounded-t-4xl">
    <section class="max-w-screen-xl mx-auto px-5 md:p-10 flex flex-col gap-10 py-20 ">
      <div class="space-y-1">
        <span class="opacity-50"> @_ My work </span> <h2 class="text-3xl">Projects</h2>
      </div>

      <ProjectCards/>
    </section>
  </div>
  

</main>
