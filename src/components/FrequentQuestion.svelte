<script>
  import ReadMoreButton from "./ReadMoreButton.svelte";
  let isMore = false;
</script>

<div class="fq">
  <div class="heading">
    <span class="category">Program conditions</span>
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
      programmes. Harbour.Space is highly recognized among innovative employers
      and is strategic partner of B.Grimm multi- industry corporation with 140
      years of history in Thailand. Together we insure students get the best
      knowledge about the current job market opportunities. We offer our
      students paid internships options during studies jointly with our
      industrial partners. Employers that hired graduates of Harbour.Space in
      the past include Google, IBM, Accenture, Typeform, Frog, and other tech
      centric companies. Our industry specific employability report could be
      provided to you separately during the admission process.
    </p>
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
    grid-row: 2/2;
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
</style>
