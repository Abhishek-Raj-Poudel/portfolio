<script>
    import riberasolutions from "../assets/riberasolutions.webp"
    import infinitydigitalagency from "../assets/infinitydigitalagency.webp"
    import hivelaya from "../assets/hivelaya.webp"
    import neaneapal from "../assets/jobportalneanepal.webp"
  import ProjectCard from "./ProjectCard.svelte";

    import jayenchy from "../assets/jayenchy.webp"
    import pmlil from "../assets/pmlil.webp"
    import nepkosh from "../assets/nepkosh.webp"
    import ayla from "../assets/ayla.webp"
    import midvalley from "../assets/midvalley.webp"
  const projects = [

    {
      link: "https://riberasolutions.com.au",
      title: "Ribera Solutions",
      picture: {
        src: riberasolutions,
        alt: "Ribera Solutions Picture",
      },
    },
{
      link: "https://www.jayenchy.com/",
      title: "Jayenchy",
      picture: {
        src: jayenchy,
        alt: "Jayenchy Jewelers",
      },
    },
{
      link: "figma",
      title: "Ayla",
      picture: {
        src: ayla,
        alt: "Jayenchy Jewelers",
        figmaLink:"https://www.figma.com/design/V9RhQRmUYWck4yhkqsc2nP/Ayla?node-id=150-46&t=XLUdEphQYuuPnjbK-1"
      },
    },
{
      link: "https://www.pmlil.com/",
      title: "Prabhu Mahalaxmi",
      picture: {
        src: pmlil,
        alt: "Prabhu Mahalaxmi",
      },
    },
{
      link: "https://jobportal.neanepal.org.np",
      title: "Nea Job Portal",
      picture: {
        src: neaneapal,
        alt: "Nea Job Portal",
      },
    },
    {
      link: "https://hivelaya.com",
      title: "Hivelaya",
      picture: {
        src: hivelaya,
        alt: "Hivelaya",
      },
    },
    {
      link: "https://infinitydigitalagency.com.np",
      title: "Infinity Digital Agency",
      picture: {
        src: infinitydigitalagency,
        alt: "Infinity Digital Agency",
      },
    },

    {
      link: "https://midvalley.edu.np/",
      title: "Midvalley College",
      picture: {
        src: midvalley,
        alt: "Midvalley Intl College",
      },
    },
    {
      link: "https://nepkosh.com",
      title: "Nepkosh",
      picture: {
        src: nepkosh,
        alt: "Nepkosh",
      },
    },

  ];
</script>

<div class="grid lg:grid-cols-2 gap-10">
  {#each projects as project}
    <ProjectCard
      link={project.link}
      title={project.title}
      picture={{
        src:project.picture.src,
        alt: project.picture.alt,
      }}
    />
  {/each}
</div>
