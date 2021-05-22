<script>
  import Fa from "svelte-fa/src/fa.svelte";
  import { faAngleUp, faAngleDown } from "@fortawesome/free-solid-svg-icons";

  export let isExpand = false;
  export let categories;
  export let faq_category = "Select an option";

  function clickHandle() {
    isExpand = !isExpand;
  }

  function handleFilter(category) {
    faq_category = category;
  }
</script>

<div class="dropdown" on:click={clickHandle}>
  <div class="title pointerCursor">
    <span>
      {faq_category}
    </span>
    {#if isExpand}
    <span class="arrow">
      <Fa icon={faAngleUp} />
    </span>
    {:else}
    <span class="arrow">
      <Fa icon={faAngleDown} />
    </span>
    {/if}
  </div>

  <div class="menu pointerCursor {isExpand ? '' : 'hide'} ">
    <div on:click={() => handleFilter("All")} class="option" id="all">All</div>
    {#each categories as category}
      <div on:click={() => handleFilter(category)} class="option" id={category}>
        {category}
      </div>
    {/each}
  </div>
</div>

<style>
  .hide {
    max-height: 0 !important;
  }

  .dropdown {
    border: 0.1em solid var(--gray-3);
    border-radius: 20px;
    width: 15em;
    padding: 10px;
    margin-bottom: 1em;
    z-index: 2;
    background-color: white;
  }

  .dropdown .title {
    display: flex;
    justify-content: space-between;
    margin: 0.3em 0.3em 0.3em 0.3em;
    width: 100%;
    color: var(--purple);
  }

  .dropdown .menu {
    transition: max-height 0.5s ease-out;
    max-height: 20em;
    overflow: hidden;
    z-index: 2;
  }

  .dropdown .menu .option {
    margin: 0.3em 0.3em 0.3em 0.3em;
    margin-top: 0.3em;
  }

  .dropdown .menu .option:hover {
    color: var(--purple)
  }

  .pointerCursor:hover {
    cursor: pointer;
  }

  .arrow { 
    margin-right: 10px;
  }

  @media (min-width: 320px) and (max-width: 767px) {
    .dropdown {
      width: 100%;
    }
  }
</style>
