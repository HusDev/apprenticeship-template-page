<script>
  import Fa from "svelte-fa/src/fa.svelte";
  import { faPlus, faMinus } from "@fortawesome/free-solid-svg-icons";

  export let isMore = false;
  function clickHandle() {
    isMore = !isMore;
  }
</script>

<div class="read-more {isMore ? 'more' : ''}" on:click={clickHandle}>
  {#if isMore}
    <Fa icon={faMinus} />
  {:else}
    <Fa icon={faPlus} />
  {/if}
</div>

<style>
  .read-more {
    display: flex;
    justify-content: center;
    align-items: center;
    color: #959595;
    width: 48px;
    height: 48px;
    border-radius: 50%;
    border: #959595 solid 1px;
    cursor: pointer;
  }

  .more {
    background-color: var(--purple);
    color: white;
    border: var(--purple) solid 1px;
  }
</style>
