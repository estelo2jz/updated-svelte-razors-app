<script>
  import globalStore from '../../stores/globalStore';
  import { fly, fade, blur} from 'svelte/transition';
  import { link } from 'svelte-routing';
  import { XIcon } from 'svelte-feather-icons';
  // itemlist
  let user = false;
</script>

<div class="cart-overlay" transition:blur>
   <div class="cart-container" transition:fly={{x:100}}>
      <div class="cart" transition:fade={{delay:400}}>
      <!-- cart header -->
        <div class="">
          <button class="btn-close" on:click="{()=>{
            globalStore.toggleItem('cart', false);
          }}">
            <XIcon size="24" />
          </button>
          <h2 class="cart-title">your bag</h2>
          <span />
        </div>
      <!-- end cart header -->
      <!-- cart items -->
      <p>cart items</p>
      <!-- end cart items -->
      <!-- cart footer -->
      <div class="cart-footer">
        {#if user}
          <a href="/checkout" use:link class="btn btn-primary btn-block"
            on:click={()=>{
            globalStore.toggleItem('cart', false);
          }}>
            checkout
          </a>
        {:else}
          <p class="cart-login">
            in order to checkout please
            <a href="/login" use:link
              on:click={()=>{
              globalStore.toggleItem('cart', false);
            }}>
              login
            </a>
          </p>
        {/if}
      </div>
      <!-- end cart footer -->
     </div>
   </div>
</div>