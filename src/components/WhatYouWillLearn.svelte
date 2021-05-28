<script lang="ts">
  import ReadMoreButton from "./ReadMoreButton.svelte";
  let isMore: boolean = false;
</script>

<div class="fq">
  <div class="heading">
    <div>
      <span class="title">Do I get a job placement upon graduation?</span>
    </div>
    <div class="toggle-btn">
      <ReadMoreButton bind:isMore />
    </div>
    <p class={isMore ? "" : "hidden"}>
      The majority of our students receive numerous job offers at the end of the
      second academic year of their Bachelor's programme and at the end of the
      first academic year of their Master's programme. The best applicants
      receive an offer from our industrial partners at the beginning of their
    </p>
  </div>
</div>

<style>
  .fq {
    border-bottom: solid 1px var(--gray-3);
    padding: 20px;
  }

  .heading {
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    cursor: pointer;
  }

  p {
    grid-column: 1/1;
    grid-row: 2/2;
    display: block;
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
    justify-self: end;
  }
</style>
