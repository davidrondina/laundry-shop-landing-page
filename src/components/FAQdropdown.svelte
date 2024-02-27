<script>
    import { slide } from "svelte/transition";

    export let q;
    let show = false;
    let buttonIcon = "fa-plus";

    function toggle() {
        show = !show;
    }

    $: buttonIcon = !show ? "fa-plus" : "fa-minus";
</script>

<div class="bg-white rounded-lg overflow-hidden shadow">
    <button
        on:click={toggle}
        class="w-full px-6 py-4 {show
            ? 'bg-sky-700 text-white'
            : 'bg-white text-neutral-900'} inline-flex justify-between gap-x-4 font-semibold hover:bg-sky-700 hover:text-white"
        ><span class="text-left">{q.question}</span>
        <span><i class="fa-solid {buttonIcon}"></i></span>
    </button>
    {#if show}
        <p transition:slide={{ duration: 300 }} class="bg-white px-6 py-4">
            {q.answer}
        </p>
    {/if}
</div>
