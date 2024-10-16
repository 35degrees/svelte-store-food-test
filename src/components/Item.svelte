<script>
  import AddItem from "./AddItem.svelte";
  export let item

</script>

<div class="item">
  <h2>{item}</h2>
  <AddItem item={item} />
</div>

<style>
  .item {
    width: 25%;
    border: 1px dotted green;
    text-align: center;
  }
</style>