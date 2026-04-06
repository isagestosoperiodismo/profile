<script>
  import { base } from "$app/paths";
  import { page } from "$app/stores";

  const normalize = (path) => (path.endsWith("/") ? path : `${path}/`);
  const withBase = (path) => `${base}${path}`;
  const isActive = (path) => normalize($page.url.pathname) === normalize(withBase(path));
  const isHome = () => normalize($page.url.pathname) === normalize(withBase("/"));
</script>

<aside
  class="w-full border-b border-neutral-200 bg-neutral-50 px-6 py-8 lg:fixed lg:left-0 lg:top-0 lg:h-screen lg:w-72 lg:border-b-0 lg:border-r lg:px-12"
>
  <div class="flex h-full flex-col justify-between">
    <div class="space-y-8">
      <nav
        class="flex flex-wrap items-center gap-3 text-[15px] text-neutral-900 lg:flex-col lg:items-start lg:gap-3"
      >
        <a
          class="hover:text-sky-700"
          class:underline={isHome()}
          class:decoration-sky-500={isHome()}
          class:decoration-2={isHome()}
          class:underline-offset-4={isHome()}
          href={withBase("/#about")}
        >
          Sobre mí
        </a>
        <span class="text-sky-600 lg:hidden">•</span>
        <a
          class="hover:text-sky-700"
          class:underline={isActive("/notas")}
          class:decoration-sky-500={isActive("/notas")}
          class:decoration-2={isActive("/notas")}
          class:underline-offset-4={isActive("/notas")}
          href={withBase("/notas/")}
        >
          Notas
        </a>
        <span class="text-sky-600 lg:hidden">•</span>
        <a
          class="hover:text-sky-700"
          class:underline={isActive("/huellas")}
          class:decoration-sky-500={isActive("/huellas")}
          class:decoration-2={isActive("/huellas")}
          class:underline-offset-4={isActive("/huellas")}
          href={withBase("/huellas/")}
        >
          Huellas
        </a>
        <span class="text-sky-600 lg:hidden">•</span>
        <a
          class="hover:text-sky-700"
          class:underline={isActive("/registro")}
          class:decoration-sky-500={isActive("/registro")}
          class:decoration-2={isActive("/registro")}
          class:underline-offset-4={isActive("/registro")}
          href={withBase("/registro/")}
        >
          Registro
        </a>
      </nav>

      <div class="space-y-2 text-sm text-neutral-700">
        <a
          class="block underline decoration-sky-500 decoration-2 underline-offset-4 hover:text-sky-700"
          href="https://instagram.com/igestoso"
          target="_blank"
          rel="noreferrer"
        >@igestoso</a>
        <a
          class="block underline decoration-sky-500 decoration-2 underline-offset-4 hover:text-sky-700"
          href="mailto:isagestososter@gmail.com"
        >isagestososter@gmail.com</a>
      </div>
    </div>
  </div>
</aside>


