<script>
  import ReadMoreButton from "./ReadMoreButton.svelte";
  let isMore = false;
  export let faq;
  faq.answer.forEach(ans => {
    ans["id"] = '_' + Math.random().toString(36).substr(2, 9);  
  });
</script>

<div class="fq">
  <div class="heading">
    <span class="category">{faq.type}</span>
    <div>
      <span class="title">{faq.question}</span>
    </div>
    <div class="toggle-btn">
      <ReadMoreButton bind:isMore />
    </div>
    {#each faq.answer as ans (ans.id)}
      <p key={ans.id} class={isMore ? "" : "hidden"}>
        {ans.data}
      </p> <br>
    {/each}
  </div>
</div>

<style>
  .fq {
    border-bottom: solid 1px var(--gray-3);
    padding: 20px 0;
  }

  .heading {
    display: grid;
    grid-template-columns: 2fr 4fr 1fr;
    align-items: center;
    cursor: pointer;
  }

  p {
    grid-column: 2/2;
    display: block;
  }

  .category {
    color: var(--purple);
  }

  .title {
    font-weight: 500;
    font-size: large;
    color: var(--gray-1);
  }

  .hidden {
    display: none;
  }
  .toggle-btn {
    display: flex;
    justify-content: flex-end;
  }

  @media (min-width: 320px) and (max-width: 767px) {
    .category {
      display: none;
    }

    .heading {
      grid-template-columns: 4fr 1fr;
    }
    p {
      grid-column: 1/2;
    display: block;
    }
  }
</style>
