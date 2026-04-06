<script>
  let { data } = $props();
</script>

<div>
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
            loading="lazy"
            decoding="async"
          />
        </a>
        <div class="flex items-start">
          <a
            class="text-neutral-900 hover:text-sky-700 hover:underline hover:decoration-sky-500 hover:decoration-2 hover:underline-offset-4"
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
