<script lang="ts">
    import { slide } from "svelte/transition";
    import Skills from "./Skills.svelte";
    import Socials from "./Socials.svelte";

    let showMore = $state(false);
</script>

<article
    class="p-8 bg-white/10 backdrop-blur rounded-xl w-full space-y-5"
    style="box-shadow: 0px 18px 88px -4px rgba(24,39,75,0.05);"
>
<div class="hidden md:block">
   <Socials/> 
</div>
    <!-- Title and position -->
    <div class="space-y-1">
        <h1 class="text-xl md:text-2xl font-bold">Abhishek Raj Poudel</h1>
        <h2 class="opacity-60 font-semibold">Full-Stack Developer</h2>
    </div>
<div class=" md:hidden">
   <Socials/> 
</div>
    <!-- SKILLS -->
    <div class="hidden md:block">
        <Skills />
    </div>

    {#if showMore}
        <button
            onclick={() => (showMore = false)}
            class="flex items-center w-full text-sm uppercase text-center gap-2 cursor-pointer hover:bg-black/5 hover:scale-95 duration-300 py-2 rounded-xl"
            transition:slide={{ duration: 300 }}
        >
            <span class="flex-grow border-t border-black border-dashed"></span>
            Less Info
            <span class="inline-block transform rotate-[-90deg]">~></span>
            <span class="flex-grow border-t border-black border-dashed"></span>
        </button>
        <div class="md:hidden">
            <Skills />
        </div>
        <div class="flex flex-col gap-4">
            <h2 class="text-xl">Experiences</h2>
            <div
                class="flex gap-5 justify-between border-b border-black/5 py-4"
            >
                <div class="flex gap-2">
                    <div class="flex flex-col gap-1">
                        <h3 class="">Digital Co-Ordinator</h3>
                        <p class="text-sm uppercase text-black/50 font-medium">
                            Infinity Development Enterprise
                        </p>
                    </div>
                </div>

                <p class="text-sm uppercase text-black/50 font-medium">
                    2025-Present
                </p>
            </div>
            <div
                class="flex gap-5 justify-between border-b border-black/5 py-4"
            >
                <div class="flex gap-2">
                    <div class="flex flex-col gap-1">
                        <h3 class="">Full-Stack Developer</h3>
                        <p class="text-sm uppercase text-black/50 font-medium">
                            Infinity Development Enterprise
                        </p>
                    </div>
                </div>

                <p class="text-sm uppercase text-black/50 font-medium">
                    2024-2025
                </p>
            </div>

            <div
                class="flex gap-5 justify-between border-b border-black/5 py-4"
            >
                <div class="flex gap-2">
                    <div class="flex flex-col gap-1">
                        <h3 class="">Front-End Developer</h3>
                        <p class="text-sm uppercase text-black/50 font-medium">
                            Infinity Development Enterprise
                        </p>
                    </div>
                </div>

                <p class="text-sm uppercase text-black/50 font-medium">
                    2023-2024
                </p>
            </div>
            <div
                class="flex gap-5 justify-between border-b border-black/5 py-4"
            >
                <div class="flex gap-2">
                    <div class="flex flex-col gap-1">
                        <h3 class="">Front-End Intern</h3>
                        <p class="text-sm uppercase text-black/50 font-medium">
                            Infinity Development Enterprise
                        </p>
                    </div>
                </div>

                <p class="text-sm uppercase text-black/50 font-medium">2023</p>
            </div>
        </div>
    {/if}
</article>
<button
    onclick={() => (showMore = !showMore)}
    class="bg-black/5 rounded-b-xl px-5 py-1 w-4/5 uppercase text-sm cursor-pointer hover:bg-black/10 hover:scale-95 duration-300"
>
    {#if !showMore}
        More Info <span class="inline-block transform rotate-[90deg]">~></span>
    {:else}
        Less Info
        <span class="inline-block transform rotate-[-90deg]">~></span>
    {/if}
</button>
