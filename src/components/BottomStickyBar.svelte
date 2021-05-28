<script lang="ts">
  import Countdown from "svelte-countdown";

  export let company: string;
  export let location: string;
  export let duration: number;
  export let scholarship_start_date: string;
  export let application_end_date: string;
</script>

<div class="stickyBar">
  <div class="properity">
    <span class="title">{company}</span>
    <span class="value">Data Science</span>
  </div>
  <div class="properity">
    <span class="title">Location</span>
    <span class="value">{location}</span>
  </div>
  <div class="properity">
    <span class="title">Duration</span>
    <span class="value">{duration} Year Full-Time</span>
  </div>
  <div class="properity">
    <span class="title">Start date</span>
    <span class="value">{scholarship_start_date}</span>
  </div>
  <div class="properity">
    <span class="title">Application deadline</span>
    <span class="value">{application_end_date}</span>
  </div>
  <div class="properity">
    <span class="title">Application closes in</span>
    <Countdown
      from={application_end_date}
      format="YYYY-MM-DD H:m:s"
      zone="CEST"
      let:remaining
    >
      <span class="value"
        >{remaining.days} Day : {remaining.hours} Hrs : {remaining.minutes} Min :
        {remaining.seconds} Seg</span
      >
    </Countdown>
  </div>
</div>

<style>
  .stickyBar {
    display: grid;
    grid-template-columns: repeat(6, 1fr);
    row-gap: 20px;
    padding: 20px;
    justify-content: space-around;
    background-color: white;
    border: var(--gray-3) solid 1px;
    position: fixed;
    width: 100%;
    bottom: 0;
    z-index: 5;
  }

  .properity {
    display: flex;
    flex-direction: column;
  }

  .title {
    margin-bottom: 10px;
    color: var(--gray-1);
  }

  .value {
    color: var(--gray-2);
  }

  @media (min-width: 320px) and (max-width: 1024px) {
    /* CSS */
    .stickyBar {
      grid-template-columns: repeat(3, 1fr);
      padding: 10px;
    }

    span {
      font-size: small;
    }
  }
</style>
