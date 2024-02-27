<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import Card from "./Card.svelte";
    import ReviewDetail from "./ReviewDetail.svelte";

    let reviews = [
        {
            profile: "assets/woman.jpg",
            name: "Nina Williams",
            occupation: "Housewife",
            comment:
                "The process is so convenient, and I saved a lot of time. They indeed made my laundry dreams come true!",
        },
        {
            profile: "assets/man.jpg",
            name: "John Doe",
            occupation: "Company worker",
            comment:
                "Due to busy work, I've always had no time to do my laundry. But with the help of WishWashers, I don't have to worry about my laundry, and I can now do other stuff.",
        },
        {
            profile: "assets/man-2.jpg",
            name: "Jobas Jalapers",
            occupation: "Livestreamer",
            comment:
                "As a full-time livestreamer, I have to keep my audiences entertained. I don't have to do my laundry anymore because of Wishwashers. They are the best!",
        },
    ];
</script>

<SectionWrapper>
    <div class="py-16 px-8 md:px-16">
        <h2
            class="mb-16 font-bold text-neutral-900 text-3xl text-center uppercase"
        >
            What our <span class="text-sky-700">customers</span> say
        </h2>

        <ul
            data-aos="fade-up"
            data-aos-duration="600"
            class="grid grid-cols-1 gap-y-5 md:gap-y-0 md:grid-cols-3 gap-x-5"
        >
            {#each reviews as review}
                <Card>
                    <ReviewDetail {review} />
                </Card>
            {/each}
        </ul>
    </div>
</SectionWrapper>
