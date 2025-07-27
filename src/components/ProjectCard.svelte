<script lang="ts">
    import { fly } from "svelte/transition";
    let { link, title, picture } = $props();
    let show = $state(false);
    const displayLink = link?.replace(/^https?:\/\//, "");

    function inView(node: HTMLElement) {
        const observer = new IntersectionObserver(
            ([entry]) => {
                if (entry.isIntersecting) {
                    show = true;
                    observer.disconnect(); // Only animate once
                }
            },
            {
                threshold: 0.1, // Trigger when 10% visible
            },
        );

        observer.observe(node);

        return {
            destroy() {
                observer.disconnect();
            },
        };
    }
</script>

<div use:inView>
    {#if show}
<a
    href={link.toLowerCase() === 'figma' ? picture.figmaLink : link}
    class="group hover:shadow-lg bg-white px-1 pb-1 flex flex-col rounded-2xl duration-300"
    transition:fly={{ y: 50, opacity: 0, duration: 300 }}
>
            <!-- Header with title and link -->
            <div class="flex justify-between items-center gap-5 py-4 px-3">
                <h3 class="hidden md:block lg:hidden xl:block text-sm">
                    {title}
                </h3>
                <p
                    class="px-4 py-1 rounded-full backdrop-blur-lg bg-black/5 text-xs h-fit"
                >
                    <span>{displayLink}</span>
                    {#if link.toLowerCase() !== 'figma'}
                    <span class="inline-block transform rotate-[-45deg]"
                        >~></span >
                    {/if}
                </p>
            </div>

            <!-- Image window -->
            <div class="flex items-end bg-black/5 rounded-xl pt-10 h-full">
                <div
                    class="px-[3px] pb-[3px] w-4/5 bg-white rounded-t-xl mx-auto h-[300px] overflow-hidden"
                >
                    <!-- Mac Navbar -->
                    <div class="py-2 px-[9px] flex gap-0.5">
                        <div class="size-[6px] bg-red-400 rounded-full"></div>
                        <div class="size-[6px] bg-amber-400 rounded-full"></div>
                        <div class="size-[6px] bg-green-400 rounded-full"></div>
                    </div>
                    <div class="rounded-t-xl overflow-hidden">
                        <img
                            src={picture.src}
                            class="object-cover w-full"
                            loading="lazy"
                            alt={picture.alt}
                        />
                    </div>
                </div>
            </div>
        </a>
    {/if}
</div>
