<script>
    export let service;
</script>

<li class="group flex-1 flex flex-col items-center gap-y-8">
    <div class="w-[250px] rounded-lg overflow-hidden">
        <div class="solid-gradient flex items-center">
            <div
                class="bg-sky-600 group-even:bg-neutral-600 mx-auto w-32 h-32 rounded-full flex justify-center items-center"
            >
                <img src={service.image} alt="An icon describing the service" />
            </div>
        </div>

        <div class="bg-white py-6">
            <h4 class="font-bold text-xl uppercase">{service.name}</h4>
        </div>
    </div>
</li>

<style>
    .solid-gradient {
        background: linear-gradient(
            to bottom,
            #e0f2fe 0%,
            #e0f2fe 50%,
            white 50%,
            white 100%
        );
    }
</style>
