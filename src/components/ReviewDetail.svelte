<script>
    export let review;
</script>

<div class="flex gap-x-4">
    <div
        class="w-16 h-16 flex justify-center items-center rounded-full overflow-hidden"
    >
        <img
            src={review.profile}
            alt={review.name}
            class="w-full h-full object-cover object-center"
        />
    </div>
    <div class="flex flex-col justify-center">
        <p class="font-semibold text-sky-700">{review.name}</p>
        <span class="block text-neutral-600 text-sm">{review.occupation}</span>
    </div>
</div>

<p class="text-center">{review.comment}</p>
