<script>
  import p1 from "$lib/assets/p1.jpg";
  import p2 from "$lib/assets/p2.jpg";
  import p3 from "$lib/assets/p3.jpg";
  import p4 from "$lib/assets/p4.jpg";

  const projectImages = [p1, p2, p3, p4];
</script>

<div class="mt-2">
  <h2 class="text-2xl md:text-3xl">Proyectos</h2>
  <ul class="list-disc space-y-6 pl-5 pt-4">
    <li>
      Huellas de nuestra historia.<a
        class="text-blue-600 underline hover:text-blue-700"
        href="https://www.youtube.com/watch?v=g13g_nt4yXo&t=2s"
      >
        Ver</a
      >
      <p class="mt-2 text-sm text-neutral-600">
        Descripción del proyecto.
      </p>
    </li>
    <li class="list-none -ml-5">
      <div class="grid grid-cols-2 gap-3">
        {#each projectImages as src, index}
          <img
            class="h-36 w-full rounded-md object-cover"
            {src}
            alt={`Proyecto ${index + 1}`}
          />
        {/each}
      </div>
    </li>
    <li>
      Registro de despidos y cierres en empresas del Conurbano Bonaerense.<a
        class="text-blue-600 underline hover:text-blue-700"
        href="https://isagestosoperiodismo.github.io/crisis-industrial/"
      >
        Ver</a
      >
      <p class="mt-2 text-sm text-neutral-600">
        Descripción del proyecto.
      </p>
    </li>
    <li>
      Matemática para periodistas.<a
        class="text-blue-600 underline hover:text-blue-700"
        href="https://www.youtube.com/watch?v=9n8sXo2l5jE"
      >
        Ver</a
      >
      <p class="mt-2 text-sm text-neutral-600">
        Descripción del proyecto.
      </p>
    </li>
  </ul>
</div>
