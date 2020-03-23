<script>
  import globalStore from '../../stores/globalStore';
  import cart from '../../stores/cart';
  $: total = $cart.reduce((acc, curr)=>{
    return (acc += curr.amount);
  },0);

  import { ArchiveIcon } from 'svelte-feather-icons';
</script>

<!-- cart toggle -->
<div class="btn-cart-container">
  <button 
    class="btn-cart-toggle icon" 
    on:click={() => {
      globalStore.toggleItem('cart', true);
    }}>
    <ArchiveIcon 
      size="24" />
  </button>
  <span class="btn-cart-items">{total}</span>
</div>