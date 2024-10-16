<script>

  export let item

  import { itemsInCart, cartContents } from "../stores.js";
	import Item from "./Item.svelte"
  
  const addItem = () => {
    itemsInCart.update(items => items + 1)
    cartContents.update(contents => [...contents, item])
  }

</script>
<button on:click={addItem}>
  Add Item
</button>