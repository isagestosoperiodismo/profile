<script>
  import Sidebar from "../../components/Sidebar.svelte";
  import Notes from "../../components/Notes.svelte";
  import Footer from "../../components/Footer.svelte";
  import { datacontent } from "$lib/data.js";

  const data = datacontent;
</script>

<div class="relative">
  <Sidebar />

  <main class="w-full px-6 py-10 lg:ml-72 lg:px-14">
    <div class="max-w-4xl">
      <header class="space-y-3">
        <h1 class="text-4xl font-semibold text-neutral-900 md:text-5xl">
          <span class="font-serif">Algunas de las notas que más me gustaron</span
          ><span class="text-sky-600">.</span>
        </h1>
      </header>

      <section class="mt-10 border-t border-neutral-200 pt-8">
        <Notes {data} />
      </section>
    </div>
  </main>
</div>
