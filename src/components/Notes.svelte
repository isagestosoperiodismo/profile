<script>
  let { data } = $props();
</script>

<div>
  <h2 class="text-3xl font-semibold text-neutral-900 md:text-4xl">
    <span class="font-serif">Notas</span><span class="text-sky-600">.</span>
  </h2>
  <div class="flex flex-col gap-8 pt-6">
    {#each data as note}
      <article
        class="grid items-start gap-5 md:grid-cols-[minmax(160px,_32%)_1fr]"
      >
        <a
          class="block w-full max-w-xs overflow-hidden aspect-video"
          href={note.href}
          target="_blank"
          rel="noreferrer"
        >
          <img
            src={note.images[0].src}
            alt={note.images[0].caption ?? note.title}
            class="h-full w-full object-cover"
            style={`object-position: ${note.imagePosition ?? "center"}`}
          />
        </a>
        <div class="flex items-start">
          <a
            class="text-neutral-900 underline decoration-sky-500 decoration-2 underline-offset-4 hover:text-sky-700"
            href={note.href}
            target="_blank"
            rel="noreferrer"
          >
            <h3 class="text-lg font-semibold leading-tight md:text-xl">
              {note.title}
            </h3>
          </a>
        </div>
      </article>
    {/each}
  </div>
</div>
