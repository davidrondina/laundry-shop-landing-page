<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import StepContainer from "./StepContainer.svelte";

    let steps = [
        {
            id: 1,
            image: "assets/laundry-bag.png",
            title: "Drop Off",
            content:
                "Drop off your laundry clothes at our store or schedule a pickup in your home",
        },
        {
            id: 2,
            image: "assets/schedule.png",
            title: "Choose a Schedule",
            content:
                "Choose a comfortable schedule to pick up or deliver your clothes.",
        },
        {
            id: 3,
            image: "assets/courier.png",
            title: "Pick Up",
            content:
                "Pick up your clothes at our store or we can deliver them right to your home once it's done.",
        },
    ];
</script>

<SectionWrapper>
    <div class="py-16 px-8 md:px-16">
        <h2
            class="mb-16 font-bold text-neutral-900 text-4xl text-center uppercase"
        >
            Easy as <span class="text-sky-700">one, two, three</span>
        </h2>

        <ul
            data-aos="fade-up"
            data-aos-duration="600"
            class="flex flex-col gap-y-5 md:gap-y-0 md:flex-row gap-x-5 text-center"
        >
            {#each steps as step}
                <StepContainer {step} />
            {/each}
        </ul>
    </div>
</SectionWrapper>
