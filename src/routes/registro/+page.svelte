<script>
  import Sidebar from "../../components/Sidebar.svelte";
  import Footer from "../../components/Footer.svelte";
  import crisisIndustrial from "$lib/assets/crisis-industrial.jpg";

  const gallery = [crisisIndustrial];
</script>

<div class="relative">
  <Sidebar />

  <main class="w-full px-6 py-10 lg:ml-72 lg:px-14">
    <div class="max-w-4xl">
      <header class="space-y-3">
        <p class="text-sm font-semibold text-sky-600">Proyecto</p>
        <h1 class="text-4xl font-semibold text-neutral-900 md:text-5xl">
          <span class="font-serif">Crisis Industrial</span
          ><span class="text-sky-600">.</span>
        </h1>
      </header>

      <section class="mt-8 space-y-4 text-base leading-relaxed text-neutral-700">
        <p>
          <span class="font-semibold text-neutral-900">Título:</span> Registro de
          despidos y cierres en empresas del Conurbano Bonaerense
        </p>
        <p>
          <span class="font-semibold text-neutral-900">Descripción:</span> Los
          datos obtenidos corresponden a un relevamiento diario en diversos medios
          de comunicación tanto locales como nacionales. Parte de la información
          proviene de un listado NO OFICIAL del Ministerio de Producción de PBA,
          es por eso que puede estar incompleto.
        </p>
      </section>

      <section class="mt-10">
        {#each gallery as src, index}
          <img
            class="h-60 w-full object-cover sm:h-72"
            {src}
            alt={`Crisis Industrial ${index + 1}`}
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
