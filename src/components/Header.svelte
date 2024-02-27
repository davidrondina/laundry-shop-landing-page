<script>
    import { slide } from "svelte/transition";
    let show = false;
    let navBtnIcon = "fa-bars";

    const toggle = () => {
        show = !show;
    };

    $: {
        navBtnIcon = show ? "fa-xmark" : "fa-bars";
        // console.log(navBtnIcon);
    }
</script>

<header
    class="font-rubik text-neutral-900 bg-white hidden md:flex justify-between items-center py-5 px-8"
>
    <a href="/" class="font-mogi px-5 py-3 text-lg"
        ><span class="text-sky-700">Wish</span>Washers</a
    >

    <div class="hidden md:flex items-center gap-x-6">
        <nav>
            <ul class="flex gap-x-6 font-bold">
                <li>
                    <a
                        href="#home"
                        class="transition ease-in-out duration-300 px-5 py-3 hover:bg-sky-200 rounded-full"
                        >Home</a
                    >
                </li>
                <li>
                    <a
                        href="#services"
                        class="transition ease-in-out duration-300 px-5 py-3 hover:bg-sky-200 rounded-full"
                        >Services</a
                    >
                </li>
                <li>
                    <a
                        href="#pricing"
                        class="transition ease-in-out duration-300 px-5 py-3 hover:bg-sky-200 rounded-full"
                        >Pricing</a
                    >
                </li>
                <li>
                    <a
                        href="#faq"
                        class="transition ease-in-out duration-300 px-5 py-3 hover:bg-sky-200 rounded-full"
                        >FAQs</a
                    >
                </li>
            </ul>
        </nav>

        <button class="inline-flex text-sky-700 font-bold">
            <a
                href="#"
                class="transition ease-in-out duration-300 px-5 py-3 border border-sky-700 rounded-full hover:bg-sky-700 hover:text-white"
                >Book Now</a
            >
        </button>
    </div>
</header>

<!-- MOBILE -->
<header
    class="z-20 fixed top-0 left-0 w-full font-rubik text-neutral-900 bg-white py-6 px-8 block md:hidden"
>
    <div class="flex justify-between items-center">
        <a href="/" class="font-mogi font-bold py-3 text-lg"
            ><span class="text-sky-700">Wish</span>Washers</a
        >
        <div>
            <div>
                <button on:click={toggle} class="text-lg"
                    ><i class="fa-solid {navBtnIcon}"></i></button
                >
            </div>
        </div>
    </div>

    {#if show}
        <nav transition:slide={{ duration: 300 }} class="mt-4 h-screen">
            <ul class="flex flex-col gap-y-4 font-bold text-2xl">
                <li>
                    <a
                        href="#home"
                        on:click={toggle}
                        class="w-full inline-flex items-center px-5 py-2.5 hover:bg-sky-100 rounded-lg"
                        >Home<svg
                            fill="none"
                            stroke="currentColor"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            class="w-4 h-4 ml-2"
                            viewBox="0 0 24 24"
                        >
                            <path d="M5 12h14M12 5l7 7-7 7"></path>
                        </svg></a
                    >
                </li>
                <li>
                    <a
                        href="#services"
                        on:click={toggle}
                        class="w-full inline-flex items-center px-5 py-2.5 hover:bg-sky-100 rounded-lg"
                        >Services<svg
                            fill="none"
                            stroke="currentColor"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            class="w-4 h-4 ml-2"
                            viewBox="0 0 24 24"
                        >
                            <path d="M5 12h14M12 5l7 7-7 7"></path>
                        </svg></a
                    >
                </li>
                <li>
                    <a
                        href="#pricing"
                        on:click={toggle}
                        class="w-full inline-flex items-center px-5 py-2.5 hover:bg-sky-100 rounded-lg"
                        >Pricing<svg
                            fill="none"
                            stroke="currentColor"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            class="w-4 h-4 ml-2"
                            viewBox="0 0 24 24"
                        >
                            <path d="M5 12h14M12 5l7 7-7 7"></path>
                        </svg></a
                    >
                </li>
                <li>
                    <a
                        href="#faq"
                        on:click={toggle}
                        class="w-full inline-flex items-center px-5 py-2.5 hover:bg-sky-100 rounded-lg"
                        >FAQs<svg
                            fill="none"
                            stroke="currentColor"
                            stroke-linecap="round"
                            stroke-linejoin="round"
                            stroke-width="2"
                            class="w-4 h-4 ml-2"
                            viewBox="0 0 24 24"
                        >
                            <path d="M5 12h14M12 5l7 7-7 7"></path>
                        </svg></a
                    >
                </li>
                <li>
                    <a
                        href="#"
                        class="w-full inline-flex px-5 py-2.5 bg-sky-700 text-white rounded-lg"
                        >Book Now</a
                    >
                </li>
            </ul>
        </nav>
    {/if}
</header>
