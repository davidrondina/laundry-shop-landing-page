<script>
    export let step;
</script>

<li class="flex-1 h-[300px] flex flex-col items-center gap-y-8">
    <div class="w-[200px] h-[200px] mx-auto flex justify-center items-center">
        <!-- <div
            class="absolute top-0 left-1/2 translate-x-1/2 -translate-x-1/2 bg-sky-100 w-44 h-44 rounded-full shadow"
        ></div> -->
        <div
            class="w-44 h-44 bg-sky-100 flex justify-center items-center rounded-full"
        >
            <img
                src={step.image}
                alt="Step Icon"
                class="z-10 w-36 h-36 transition ease-in-out duration-150 hover:scale-105 hover:drop-shadow-xl"
            />
        </div>
    </div>
    <div>
        <h3 class="text-xl font-bold uppercase">{step.id}. {step.title}</h3>
        <p class="text-ellipsis">{step.content}</p>
    </div>
</li>
