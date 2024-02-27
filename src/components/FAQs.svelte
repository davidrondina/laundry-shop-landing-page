<script>
    import SectionWrapper from "./SectionWrapper.svelte";
    import FaQdropdown from "./FAQdropdown.svelte";

    const questions = [
        {
            id: 1,
            question: "What are your basic services?",
            answer: "We offer machine wash, hand washing, dry cleaning, ironing service and pick up/delivery in nearby areas.",
        },
        {
            id: 2,
            question:
                "What is your hours of operations and pick-up / delivery schedule?",
            answer: "Our shop opens from 9 am -9 pm, Monday through Sunday. Pick-up and delivery schedule starts from 10 am until 9 pm. No in-house pickup/delivery schedule every Sunday and selected public holiday.",
        },
        {
            id: 3,
            question: "Is there a fee for pick up and delivery request?",
            answer: "Yes, there is a fee. Pick up and the delivery fee varies.",
        },
        {
            id: 5,
            question: "What happen after you pick up my laundry?",
            answer: "After we pick up your clothes our laundry attendants will prepare and que it for washing. A notification shall be sent once your laundry is ready for delivery.",
        },
        {
            id: 6,
            question: "Do you weigh the laundry during pick up?",
            answer: "Each service has a bag assigned with allocated weight in kg. Our delivery staff shall only collect the laundry in a sealed plastic bag and shall be isolated for 2 days. The laundry attendant shall check the laundry after 2 days to confirm the weight. If there's an excess, it will be applied to another bag and will notify you if there shall be a change in your original booking.",
        },
        {
            id: 7,
            question:
                "What do I do if I have a problem with my laundry upon delivery?",
            answer: "Should there be an issue with your laundry, call us immediately and we will make every effort to resolve the matter to your satisfaction. Please understand that some issues, like persistent stains, may not be able to be resolved regardless of available products and our efforts",
        },
    ];
</script>

<SectionWrapper sectionName={"faq"}>
    <div class="bg-sky-100 py-16 px-8 md:px-16">
        <h2
            class="mb-16 font-bold text-neutral-900 text-4xl text-center uppercase"
        >
            Frequently Asked Questions
        </h2>

        <div class="flex flex-col gap-y-3">
            {#each questions as q (q.id)}
                <FaQdropdown {q} />
            {/each}
        </div>
    </div></SectionWrapper
>
