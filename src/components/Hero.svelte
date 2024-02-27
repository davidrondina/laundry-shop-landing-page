<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import heroImage from "/static/assets/hero.png";
</script>

<SectionWrapper sectionName={"home"}>
    <div
        class="bg-sky-100 py-20 px-8 md:px-16 flex flex-col gap-y-5 justify-between md:flex-row md:items-center md:gap-x-10 md:gap-y-0"
    >
        <div class="flex-1 space-y-4 order-2 md:order-1">
            <div class="space-y-2 text-center md:text-left">
                <h1 class="text-neutral-900 text-4xl md:text-6xl font-bold">
                    Where your <span class="text-sky-700">laundry</span> dreams
                    come
                    <span class="text-sky-700">true</span>
                </h1>
                <p class="text-lg md:text-base">
                    At <span class="text-sky-700">WishWashers</span>, redefine
                    your laundry with unmatched convenience and excellence.
                    Meticulous care ensures spotless, revitalized fabrics. Step
                    into a realm where each garment receives special attention
                    for a fresh, satisfying outcome. Elevate your routine with
                    us, where meticulousness meets satisfaction.
                </p>
            </div>

            <div class="text-center md:text-left">
                <button class="inline-flex text-white font-bold">
                    <a
                        href="#"
                        class="transition ease-in-out duration-300 px-5 py-3 bg-sky-700 rounded-full hover:ring-1 hover:ring-sky-700 hover:bg-transparent hover:text-sky-700"
                        >Schedule a pickup</a
                    >
                </button>
            </div>
        </div>
        <div class="flex-1 w-full h-full order-1 md:order-2">
            <img
                src={heroImage}
                alt="A woman holding laundry clothes"
                class="mx-auto"
            />
        </div>
    </div>
</SectionWrapper>
