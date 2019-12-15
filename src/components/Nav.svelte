<script>
  import Hamburger from './Hamburger.svelte';
  import NavLink from './NavLink.svelte';

  export let segment;
  let expand = false;

  function toggleMobileMenu(event) {
    expand = event.detail;
  }
</script>

<nav
  class="text-white w-full flex items-center justify-between flex-wrap
  bg-teal-500 p-6 shadow-lg lg:fixed lg:top-0">

  <a href="." class="font-semibold text-xl tracking-tight mr-4">Your Project</a>

  <div class="block lg:hidden">
    <Hamburger on:click={toggleMobileMenu} {expand} />
  </div>
  <div class="w-full block flex-grow lg:flex lg:items-center lg:w-auto">
    <div class="{!expand && 'hidden'} lg:block text-sm lg:flex-grow">
      <NavLink text="About" href="about" {segment} />
    </div>
  </div>
</nav>
