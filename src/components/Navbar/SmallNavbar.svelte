<script>
  // cart button
  import CartButton from '../Cart/CartButton.svelte';
  import { link } from 'svelte-routing';
  import { SidebarIcon } from 'svelte-feather-icons';
  // global store
  import globalStore from '../../stores/globalStore';
  let openSidebar = globalStore.toggleItem;
</script>

<nav class="navbar">
  <div class="nav-center">
    <!-- sidebar toggle -->
    <button class="btn-sidebar-toggle" 
    on:click="{()=>{
      openSidebar('sidebar', true)
    }}">
      <SidebarIcon size="24" pointer="cursor" />
    </button>
    <!-- logo -->
    <a href="/" use:link class="nav-logo">
      <img src="/assets/images/logo.svg" class="logo" alt="razors logo" />
    </a>
    <!-- cart button -->
    <CartButton /> 
  </div>
</nav>