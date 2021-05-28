<script lang="ts">
  import ReadMoreButton from "./ReadMoreButton.svelte";

  interface Answer {
    data: string;
    type: string;
  }

  interface IFaq {
    type: string;
    answer: Answer[];
    question: string;
  }

  export let faq: IFaq;
  export let faq_category: string = "All";
  let isMore: boolean = false;
  let answer: Answer[] = faq.answer;  
</script>

{#if faq_category == faq.type || faq_category == "All" || faq_category == "Select an option"}
  <div class="fq">
    <div class="heading">
      <span class="category">{faq.type}</span>
      <div>
        <span class="title">{faq.question}</span>
      </div>
      <div class="toggle-btn">
        <ReadMoreButton bind:isMore />
      </div>
      {#each answer as ans}
        <p class={isMore ? "active" : "hidden"}>
          {ans.data}
        </p>
      {/each}
    </div>
  </div>
{/if}

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
    transition: 500ms;
  }

  p.active {
    display: block;
    height: fit-content;
    opacity: 1;
    padding-bottom: 50px;
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
    display: block;
    height: 0;
    opacity: 0;
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
