<script>
  import Countdown from "svelte-countdown";
  export let application_end_date;
</script>

<Countdown
  from={application_end_date}
  format="YYYY-MM-DD H:m:s"
  zone="CEST" 
  let:remaining
>
  <div class="application-close">
    <p>Application closes in</p>
    <span>{remaining.days} Day : {remaining.hours} Hrs : {remaining.minutes} Min : {remaining.seconds} Seg</span>
  </div>
</Countdown>

<style>
  .application-close {
    padding: 20px;
    border-radius: 4px;
    border: var(--gray-3) solid 1px;
  }

  .application-close p {
    margin-top: 0;
    color: var(--purple);
    font-weight: 500;
    font-size: 16px;
  }

  .application-close span {
    color: var(--gray-1);
    font-size: 24px;
    font-weight: 300;
  }
</style>
