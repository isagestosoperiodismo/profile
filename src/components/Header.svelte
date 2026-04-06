<script>
  import { base } from "$app/paths";
  import { fade } from "svelte/transition";

  const withBase = (path) => `${base}${path}`;
</script>

<header in:fade={{ duration: 700 }} class="space-y-6">
  <p class="text-sm font-semibold text-sky-600">Hola!</p>
  <h1 class="text-4xl font-semibold leading-tight text-neutral-900 md:text-6xl">
    <span class="font-serif">Soy Isabel Gestoso</span
    ><span class="text-sky-600">.</span>
  </h1>
  <p class="text-sm leading-relaxed text-neutral-700 md:text-base">
    Periodista, fotógrafa y programadora. Escribo sobre territorio y memoria en el
    conurbano bonaerense. Publiqué en
    <a
      class="underline decoration-sky-500 decoration-2 underline-offset-4 hover:text-sky-700"
      href="https://www.clarin.com/autor/isabel-gestoso.html"
      target="_blank"
      rel="noreferrer"
    >Clarín</a>
    y
    <a
      class="underline decoration-sky-500 decoration-2 underline-offset-4 hover:text-sky-700"
      href="https://eterdigital.com.ar/author/gestoso/"
      target="_blank"
      rel="noreferrer"
    >ETER Digital</a>.
    Soy productora de
    <a
      class="underline decoration-sky-500 decoration-2 underline-offset-4 hover:text-sky-700"
      href={withBase("/huellas/")}
    >Huellas de Nuestra Historia</a>
    y escribí
    <a
      class="underline decoration-sky-500 decoration-2 underline-offset-4 hover:text-sky-700"
      href="https://revista-quorum.webnode.page/l/alex-kohan-la-verdad-no-esta-en-lo-explicito-del-humor-esta-en-lo-que-se-trafica-via-la-risa/?fbclid=PAZXh0bgNhZW0CMTEAAaaFymkUXdpgP7I3bYe_QkkvGNrCJtpGZakkAxAoBvuk1ZH_iEwi_Azlofg_aem_5AppolP2Q_-xxtBiE3ElSw"
      target="_blank"
      rel="noreferrer"
    >mi primera nota publicada</a>.
  </p>
</header>


