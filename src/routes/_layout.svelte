<script>
  import Nav from '../components/Nav.svelte';
  import Tailwindcss from '../components/Tailwind.svelte';

  export let segment;
</script>

<Tailwindcss />

<Nav {segment} />

<main class="lg:mt-20 container mx-auto p-4">
  <slot />
</main>
