<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import Card from "./Card.svelte";
    import PricingDetail from "./PricingDetail.svelte";

    let pricings = [
        {
            icon: "assets/t-shirt-2-line.svg",
            price: 'From <span class="text-accent">PHP 300.00</span> per bag',
            name: "Basic Items",
        },
        {
            icon: "assets/t-shirt-air-line.svg",
            price: 'From <span class="text-accent">PHP 150.00</span> per piece',
            name: "Dry Cleaning",
        },
        {
            icon: "assets/shirt-line.svg",
            price: 'From <span class="text-accent">PHP 30.00</span> per piece',
            name: "Special Items",
        },
    ];
</script>

<SectionWrapper sectionName={"pricing"}>
    <div class="py-16 px-8 md:px-16">
        <h2
            class="mb-16 font-bold text-neutral-900 text-4xl text-center uppercase"
        >
            Pricing
        </h2>

        <ul
            data-aos="fade-up"
            data-aos-duration="600"
            class="grid grid-cols-1 gap-y-5 md:gap-y-0 md:grid-cols-3 gap-x-5 text-center"
        >
            {#each pricings as pricing}
                <Card>
                    <PricingDetail {pricing} />
                </Card>
            {/each}
        </ul>
    </div>
</SectionWrapper>
