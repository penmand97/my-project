<script>
    import Step from "./Step.svelte";

let steps = [ 
    {
        name: "Wealth and Hellness",
        icon: "fa-solid fa-cart-shopping",
        description:
            "Wealth and Hellness is a store created with Next.js, Shopify, Stripe & Node.js and CSS. Stripe & Shopify are used for all transaction handling.",
    },
    {
        name: "DA'von Penman Portfolio",
        icon: "fa-solid fa-list-check",
            description:
                "This website links back to the current one and is a way for me DA'von Penman to show the world my work!",
        },
    {
        name: "Happy Cacti",
        icon: "fa-solid fa-cart-shopping",
        description:
            "Happy Cacti is a store created with Next.js, Shopify, Stripe & Node.js and CSS. Stripe & Shopify are used for all transaction handling.",
    },

];

let benefits = [
        {
            metric: "10x",
            name: "a self taught developer",
            description:
                "I taught myself to code using  online resources alongside my 9-5 job and absolutely fell in love with the creativity and problem solving that is involved in developing and engineering innovative new online experiences. Starting of with JavaScript, HTML & CSS and evolving my knowledge base to include JavaScript frameworks, I hope to integrate backend programming, design & cloud services. (I'm currently a certified AWS Cloud Practitioner)",
        },
        {
            name: "a fast learner",
            description:
                "Being a fast learner fuels my passion for crafting exceptional user experiences. I am always eager to learn more and I actively seek out ways to both showcase and further develop my skills",
        },
        {
            name: "an excellent communicator",
            description:
                "Communication is key and it's a paramount value of mine. I believe in transparency and constructive communication above all else. This helps me develop deep relationships with both clients and my peers and ensures my effectiveness and productivity in any work space with any team.",
        },   
];

</script>

<main class="flex flex-col flex-1 p-4">
    <section id="introPage" class="grid grid-cols-1 lg:grid-cols-2 gap-10 py-8 sm:py-14">
                <div class="flex flex-col lg:justify-center text-center lg:text-left gap-6 md:gap-8 lg:gap-10">
                
                    <h2 class="font-semibold text-4xl sm:text-5xl md:text-6xl">
                    Hi! I'm <span class="poppins text-violet-400"> DA'von</span> Penman <br/> 
                    Full Stack <span class="poppins text-violet-400"> Developer </span>
                    </h2>

                <p class="text-base sm:text-lg md:text-xl">
                My <span class="text-violet-400"> favorite tech </span> (at the moment) includes JavaScript (NEXT.js or Sveltekit), TailwindCSS & Node.js 
                </p>
    
    
    
                <a
                class="blueShadow mx-auto lg:mr-auto lg:ml-0 text-base sm:text-lg md:text-xl 
                poppins relative overflow-hidden px-6 py-3 group rounded-full bg-white 
                text-slate-950 cursor-pointer" 
                href="https://www.linkedin.com/in/davonpenman/"
                target="_blank" >


                <div class="absolute top-0 right-full w-full h-full bg-violet-400 
                opacity-20 group-hover:translate-x-full z-0 duration-200"/>

                    <h4 class="relative z-9">Get in touch &rarr;</h4>
                </a>
            </div>
            <div class="relative shadow-2xl grid place-items-center">
                <!-- svelte-ignore a11y-img-redundant-alt -->
                <img src={"/Users/dav/my-project/static/images/profile.png"}
                alt="Profile image"
                class="object-cover z-[2] max-h-[70vh]"/>

            </div>
    </section>

    <section class="py-20 lg:py-32 flex flex-col gap-24" id="projects">
        <div class="flex flex-col gap-2 text-center">
            <h6 class="text-large sm:text-xl md:text-2xl">
                A few of my creative endeavors.
            </h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl">
                Curious to <span class="poppins text-violet-400">see</span> my work?
            </h3>
        </div>
        <a
            href="https://www.youtube.com/watch?v=dQw4w9WgXcQ"
            target="_blank"
            class="mx-auto px-4 py-2 rounded-md border border-solid border-white flex items-center gap-2 -mb-4 sm:-mb-0 -mt-10 hover:border-violet-700 duration-200"
        >
            <i class="fa-regular fa-circle-play" />
            <p>Watch the video</p>
        </a>
        <div class="grid grid-cols-1 lg:grid-cols-3 gap-12 lg:gap-10">
            <Step step={steps[0]}>
                <p>
                    Wealth and Hellness is an ecommerce fashion brand created with <strong
                        class="text-violet-400"
                        > Next.js, Shopify, Stripe & Node.js + CSS</strong> 
                </p>
            </Step>
            <Step step={steps[1]}>
                <p>
                    This Portfolio allows me to show the world my work, created with <strong
                        class="text-violet-400"
                        > Next.js, TailwindCSS, Node.js + CSS and SvelteKit</strong> 
                </p>
            </Step>
            <Step step={steps[2]}>
                <p>
                    Happy Cacti is an online ecommerce store focused on greeting cards and gifts created with <strong
                        class="text-violet-400"
                        > Next.js, Shopify, Stripe & Node.js + CSS</strong> 
                </p>
            </Step>

        </div>
    </section>
   <section id="about" class="py-20 pt-10 lg:pt-16 lg:py-32 flex flex-col gap-16 sm:gap-20 md:gap-24 relative">
        <div
        class="flex flex-col gap-2 text-center relative before:absolute before:top-0 before:left-0 before:w-2/3 before:h-1.5 
        before:bg-violet-700 after:absolute
        after:bottom-0 after:right-0 after:w-2/3 after:h-1.5 after:bg-violet-700 py-4">
            <h6 class="text-large sm:text-xl md:text-2xl">Want to know more?</h6>
            <h3 class="font-semibold text-3xl sm:text-4xl md:text-5xl"> A bit <span class="poppins text-violet-400">about</span> me.</h3>
        </div>


        <p class="mx-auto poppins font-semibold text-lg sm:text-xl md:text-2xl">
            I am . . .
        </p>
        <div class="flex flex-col gap-20 w-full mx-auto max-w-[800px]">
            {#each benefits as benefit, index}

            <div class="flex gap-6 sm:gap-8">
            <p
                class="poppins text-4xl sm:text-5xl md:text-6xl text-slate-500 font-semibold"
            >
                0{index + 1}
            </p>
            <div class="flex flex-col gap-6 sm:gap-8">
                <h3 class="text-2xl sm:text-3xl md:text-5xl">
                    {benefit.name}
                </h3>
                <p>{benefit.description}</p>
            </div>
          </div>
         {/each}


        
        </div>



    </section>


</main>