<script>
  import Sidebar from "../../components/Sidebar.svelte";
  import Footer from "../../components/Footer.svelte";
  import p1 from "$lib/assets/p1.jpg";
  import p2 from "$lib/assets/p2.jpg";
  import p3 from "$lib/assets/p3.jpg";
  import p4 from "$lib/assets/p4.jpg";

  const gallery = [p1, p2, p3, p4];
</script>

<div class="relative">
  <Sidebar />

  <main class="w-full px-6 py-10 lg:ml-72 lg:px-14">
    <div class="max-w-4xl">
      <header class="space-y-3">
        <p class="text-sm font-semibold text-sky-600">Proyecto</p>
        <h1 class="text-4xl font-semibold text-neutral-900 md:text-5xl">
          <span class="font-serif">Huellas de nuestra historia</span
          ><span class="text-sky-600">.</span>
        </h1>
      </header>

      <section class="mt-8 space-y-4 text-base leading-relaxed text-neutral-700">
        <p>
          Lo que archivamos mantiene viva la memoria, nos permite revisar el pasado
          para aprender y comprender el presente. Resguardar y mantener archivos es
          una tarea fundamental para la construcción del futuro. ¿Quién se encarga
          de eso? ¿Cómo se hace? En Huellas de la historia damos respuesta a esas
          preguntas.
        </p>
        <div>
          <p class="font-semibold text-neutral-900">CON LA PARTICIPACIÓN DE:</p>
          <p class="mt-3">
            Valeria Mustoni<br />
            Arturo Aguirre<br />
            María Belén Correa<br />
            Daniela Drucaroff<br />
            Emiliano Meincke<br />
            Lautaro Pérez Miranda<br />
            Ana Laura Masiello
          </p>
        </div>
      </section>

      <section class="mt-10 grid gap-4 sm:grid-cols-2">
        {#each gallery as src, index}
          <img
            class="aspect-square w-full max-w-xs justify-self-center object-cover"
            {src}
            alt={`Huellas de nuestra historia ${index + 1}`}
          />
        {/each}
      </section>

      <div class="mt-10">
        <a
          class="inline-flex items-center gap-2 text-sm font-semibold text-neutral-900 underline decoration-sky-500 decoration-2 underline-offset-4 hover:text-sky-700"
          href="https://www.youtube.com/watch?v=g13g_nt4yXo&t=2s"
          target="_blank"
          rel="noreferrer"
        >
          Ver proyecto
        </a>
      </div>
    </div>
  </main>
</div>
