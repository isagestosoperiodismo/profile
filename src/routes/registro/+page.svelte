<script>
  import Sidebar from "../../components/Sidebar.svelte";
  import Footer from "../../components/Footer.svelte";
  import img2 from "$lib/assets/2.jpg";
  import img4 from "$lib/assets/4.jpg";
  import img5 from "$lib/assets/5.jpg";

  const gallery = [img2, img4, img5];
</script>

<div class="relative">
  <Sidebar />

  <main class="w-full px-6 py-10 lg:ml-72 lg:px-14">
    <div class="max-w-4xl">
      <header class="space-y-3">
        <p class="text-sm font-semibold text-sky-600">Proyecto</p>
        <h1 class="text-4xl font-semibold text-neutral-900 md:text-5xl">
          <span class="font-serif">Registro de despidos PBA</span
          ><span class="text-sky-600">.</span>
        </h1>
      </header>

      <section class="mt-8 space-y-4 text-base leading-relaxed text-neutral-700">
        <p>
          Este espacio sirve para describir el contexto del registro, el recorte
          territorial y el impacto social que buscás visibilizar.
        </p>
        <p>
          Podés sumar datos, fuentes y decisiones editoriales para explicar cómo se
          construyó el proyecto y qué aporta.
        </p>
      </section>

      <section class="mt-10 grid gap-4 sm:grid-cols-3">
        {#each gallery as src, index}
          <img
            class="h-44 w-full object-cover"
            {src}
            alt={`Registro de despidos ${index + 1}`}
          />
        {/each}
      </section>

      <div class="mt-10">
        <a
          class="inline-flex items-center gap-2 text-sm font-semibold text-neutral-900 underline decoration-sky-500 decoration-2 underline-offset-4 hover:text-sky-700"
          href="https://isagestosoperiodismo.github.io/crisis-industrial/"
          target="_blank"
          rel="noreferrer"
        >
          Ver proyecto
        </a>
      </div>
    </div>
  </main>
</div>
