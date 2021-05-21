<script>
  export let effort; 
  export let description;
  export let title; 
</script>

<div class="commitment-card">
  <span class="title">{title}</span>
  {#if effort != ""}
  <span class="effort">{effort} hours / day</span>
  <div class="line" />
  {/if}
  <p>
   {description}
  </p>
</div>

<style>
  .commitment-card {
    display: flex;
    flex-direction: column;
    padding: 30px 20px;
    border: var(--gray-3) solid 1px;
    border-radius: 4px;
    height: 100%;
  }

  .title {
    color: var(--purple);
    margin-bottom: 10px;
    font-weight: 500;
    font-size: medium;
  }

  .effort {
    font-size: x-large;
    font-weight: 300;
    color: var(--gray-2);
    margin-bottom: 20px;
  }

  p {
    font-weight: 300;
    color: var(--gray-2);
  }

  .line {
    border-bottom: solid 1px var(--gray-3);
    width: 20px;
  }
</style>
