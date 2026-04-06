<script>
  import Header from "../components/Header.svelte";
  import Sidebar from "../components/Sidebar.svelte";
  import pic from "$lib/assets/pic.jpg";
</script>

<div class="relative bg-white">
  <Sidebar />

  <main class="w-full px-6 py-12 lg:ml-72 lg:px-14">
    <div class="max-w-4xl">
      <section
        id="about"
        class="grid items-start gap-12 lg:grid-cols-[minmax(0,1.1fr)_minmax(0,0.9fr)]"
      >
        <Header />
        <div class="space-y-3">
          <img
            class="aspect-square w-full max-w-xs object-cover grayscale"
            src={pic}
            alt="Isabel Gestoso"
            loading="eager"
            decoding="async"
            fetchpriority="high"
          />
        </div>
      </section>
    </div>
  </main>
</div>
