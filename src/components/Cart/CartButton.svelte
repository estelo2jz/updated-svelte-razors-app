<script>
  import globalStore from '../../stores/globalStore';
  import { ArchiveIcon } from 'svelte-feather-icons';
</script>

<!-- cart toggle -->
<div class="btn-cart-container">
  <button 
    class="btn-cart-toggle icon" 
    on:click={() => {
      console.log('hello');
      globalStore.toggleItem('cart', true);
    }}>
    <i class="fas fa-cart" />
    <ArchiveIcon size="24" />
  </button>
  <span class="btn-cart-items">100</span>
</div>