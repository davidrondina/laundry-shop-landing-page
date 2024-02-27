<script>
    export let pricing;
</script>

<div class="flex gap-x-4 md:gap-x-0 md:flex-col items-center">
    <div><img src={pricing.icon} alt="" /></div>
    <div class="flex flex-col items-center">
        <h4 class="text-xl font-bold">{@html pricing.price}</h4>
        <p>{pricing.name}</p>
        <a href="#" class="group mt-4 inline-flex items-center text-accent"
            ><span class="underline group-hover:no-underline">Book Now</span>
            <svg
                fill="none"
                stroke="currentColor"
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                class="w-4 h-4 ml-2"
                viewBox="0 0 24 24"
            >
                <path d="M5 12h14M12 5l7 7-7 7"></path>
            </svg>
        </a>
    </div>
</div>
