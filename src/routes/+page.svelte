<script>
  import { itemsInCart, totalPrice, cartContents } from "../stores.js";

  import Item from "../components/Item.svelte";
  let inventory = ['apples','peaches','bananas','leeks','turnips','berries']
</script>

<main>
  <div class = "items">
    {#each inventory as item}
      <Item item={item}/>
    {/each}
  </div>

  <p>There are { $itemsInCart } items in your cart.</p>
  <p>Cart total: ${ $totalPrice }</p>
  <p>Cart contents:</p>
        
  <ol>
    {#each $cartContents as item}
      <li>{item}</li>
    {/each}
  </ol>
</main>






<style>

  .items {
    display: flex;
    flex-direction: row;
  }
</style>