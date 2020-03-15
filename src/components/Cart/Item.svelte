<script>
  export let id;
  export let image;
  export let title;
  export let price;
  export let amount;
  // import cart methods
  // icons
  import { ChevronUpIcon, ChevronDownIcon } from 'svelte-feather-icons';
</script>

<!-- cart item -->
<div class="cart-item">
  <img src="{image}" alt={title} />
  <div>
    <h4>{title}</h4>
    <h5>${price}</h5>
    <button class="cart=btn remove-btn" on:click="{()=>{
      console.log('remove item')
    }}">
      remove
    </button>
  </div>
  <div>
    <button class="cart=btn amount-btn" on:click="{()=>{
      console.log('increase item')
    }}">
      <ChevronUpIcon size="24" />
    </button>
    <p class="item-amount">{amount}</p>
    <button class="cart=btn amount-btn" on:click="{()=>{
      console.log('decrease item')
    }}">
      <ChevronDownIcon size="24" />
    </button>
  </div>
</div>