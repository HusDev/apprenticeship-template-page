<script>
    import Fa from "svelte-fa/src/fa.svelte";
    import { faAngleUp, faAngleDown } from "@fortawesome/free-solid-svg-icons";
  
    export let isExpand = false;
    function clickHandle() {
      isExpand = !isExpand;
    }
  </script>

<div class="dropdown" on:click={clickHandle}>
  <div class="title pointerCursor">
     Select an option
    {#if isExpand }
     <Fa icon={faAngleUp} />
    {:else}
    <Fa icon={faAngleDown} />
    {/if}
    </div>

  <div class="menu pointerCursor {isExpand? "": "hide"} ">
    <div class="option" id="option1">Option 1</div>
    <div class="option" id="option2">Option 2</div>
    <div class="option" id="option3">Option 3</div>
    <div class="option" id="option4">Option 4</div>
    <div class="option" id="option5">Option 3</div>
    <div class="option" id="option6">Option 4</div>
  </div>
</div>

<style>
  .hide {
    max-height: 0 !important;
  }

  .dropdown {
    border: 0.1em solid var(--gray-3);
    border-radius: 20px;
    width: 10em;
    padding: 10px;
    margin-bottom: 1em;
    z-index: 2;
  }

  .dropdown .title {
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
    background: rgba(0, 0, 0, 0.2);
  }

  .pointerCursor:hover {
    cursor: pointer;
  }
</style>
