<script>
  import Fa from "svelte-fa/src/fa.svelte";
  import { faAngleUp, faAngleDown } from "@fortawesome/free-solid-svg-icons";

  export let isExpand = false;
  function clickHandle() {
    isExpand = !isExpand;
  }
</script>

<div on:click={clickHandle} class="dropdown {isExpand ? 'expand' : ''}">
  <span>All</span>
  {#if isExpand}
    <Fa icon={faAngleUp} />
  {:else}
    <Fa icon={faAngleDown} />
  {/if}
  <div class="dropdown-content {isExpand ? 'active' : ''}">
    <p>Hello World!</p>
    <p>Hello World!</p>
    <p>Hello World!</p>
    <p>Hello World!</p>
  </div>
</div>

<style>
  .dropdown {
    position: relative;
    display: flex;
    justify-content: space-between;
    width: 200px;
    padding: 15px;
    border: var(--gray-3) solid 1px;
    border-radius: 30px;
    color: var(--purple);
    cursor: pointer;
    z-index: 2;
    background-color: white;
  }

  .dropdown-content {
    display: none;
    position: absolute;
    min-width: 160px;
    padding-top: 10px;
    z-index: 3;
  }

  .active {
    display: block;
  }

  .expand {
    border-radius: 25px;
    height: 200px;
  }
</style>
