<script>
    import resume from "../assets/AbhishekPoudelResume.pdf"
    import linkedin from "../assets/linkedin.svg"
    import file from "../assets/file.svg"
    import github from "../assets/github.svg"
    import mail from "../assets/mail.svg"
</script>

<div class="flex flex-wrap gap-4  md:justify-end">
        <a
            href={resume}
            class="uppercase rounded-3xl backdrop-blur-lg bg-black/5 hover:bg-black/20 flex items-center justify-center gap-2 text-sm px-4 py-2 hover:scale-95 duration-300 w-full md:w-fit"
            target="_blank"
        >
            <img src={file} alt="Download CV" class="size-5" >
            <span class="underline"> Download CV </span>
        </a>
        
        <a
            class="uppercase rounded-3xl backdrop-blur-lg bg-black/5 hover:bg-black/20 flex items-center justify-center gap-2 text-sm px-4 py-2 hover:scale-95 duration-300 w-full md:w-fit"
            href="https://github.com/Abhishek-Raj-Poudel"
            target="_blank"
        >
            <img src={github} alt="github" class="size-5" >
            <span class="underline"> Github </span>
        </a>
        <a
        class="uppercase rounded-3xl backdrop-blur-lg bg-black/5 hover:bg-black/20 flex items-center justify-center gap-2 text-sm px-4 py-2 hover:scale-95 duration-300 w-full md:w-fit"
        href="https://www.linkedin.com/in/abhishek-raj-poudel/"
        target="_blank"
        >
        <img src={linkedin} alt="linkedin" class="size-5" >
        <span class="underline">LinkedIn</span>
        </a>

        <a
            class="btn rounded-3xl gap-2 w-full md:w-fit"
            href="mailto:abhishekrajpoudel@gmail.com"
            target="_blank"
        >
        <img src={mail} alt="contact" class="size-5 text-white" >
            <span class="underline"> Contact Me </span>
        </a>
    </div>
