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
    <ArchiveIcon size="24" />
  </button>
  <span class="btn-cart-items">10</span>
</div>