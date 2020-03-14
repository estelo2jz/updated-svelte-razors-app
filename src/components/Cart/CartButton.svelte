<script>
  import globalStore from '../../stores/globalStore';
  import FaShoppingCart from 'svelte-icons/fa/FaShoppingCart.svelte';
</script>

<!-- cart toggle -->
<div class="btn-cart-container icon">
  <button 
    class="btn-cart-toggle" 
    on:click={() => {
      console.log('hello');
      globalStore.toggleItem('cart', true);
    }}>
    <FaShoppingCart />
  </button>
  <span class="btn-cart-items">100</span>
</div>

<style>
  .icon {
    color: red;
    width: 312px;
    height: 312px;
  }
</style>