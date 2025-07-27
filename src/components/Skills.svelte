<script lang="ts">
const SKILLS = [
    "HTML",
    "CSS",
    "Javascript",
    "Tailwind CSS",
    "React",
    "Laravel",
    "Figma",
    "Wordpress",
];
</script>

<div class="flex flex-col gap-2">
    <h2>
        <span class="opacity-50 text-sm"> @_ Skills </span>
    </h2>
<div class="flex flex-wrap gap-2">
{#each SKILLS as skill}
<span
class="px-4 py-2 border rounded-full opacity-50 border-black/50 text-sm uppercase font-medium"
>{skill}</span
>
{/each}
</div>
</div>
