<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import ServiceCard from "./ServiceCard.svelte";

    let services = [
        {
            image: "assets/washing-machine.png",
            name: "Washing",
        },
        {
            image: "assets/iron.png",
            name: "Iron",
        },
        {
            image: "assets/shirt.png",
            name: "Dry Clean",
        },
        {
            image: "assets/delivery.png",
            name: "Pickup/Delivery",
        },
    ];
</script>

<SectionWrapper sectionName={"services"}>
    <div class="bg-sky-100 py-16 px-8 md:px-16">
        <h2
            class="mb-16 font-bold text-neutral-900 text-4xl text-center uppercase"
        >
            Our <span class="text-sky-700">Services</span>
        </h2>

        <ul
            data-aos="fade-up"
            data-aos-duration="600"
            class="flex flex-col flex-wrap gap-y-5 md:gap-y-0 md:gap-5 md:flex-row text-center"
        >
            {#each services as service}
                <ServiceCard {service} />
            {/each}
        </ul>
    </div>
</SectionWrapper>
