<script>
  export let location;
  export let duration;
  export let start_date;
  export let application_end_date;

  // change date 
  function handleDate(start_date) {
    let date = new Date(start_date).toDateString();
    date = date.substr(4).split(" ");
    console.log(date)
    let temp = date[0];
    date[0] = date[1]; 
    date[1] = temp;
    date = date.join(" ");
    return date;  
  }

</script>

<div class="info-card">
  <div>
    <span class="title">Location</span>
    <span class="value">{location}</span>
  </div>
  <div>
    <span class="title">Duration</span>
    <span class="value">{duration} Year</span>
    <span class="value">Full Time</span>
  </div>
  <div>
    <span class="title">Application Deadline</span>
    <span class="value">{handleDate(application_end_date)}</span>
  </div>
  <div>
    <span class="title">Start Date</span>
    <span class="value">{handleDate(start_date)}</span>
  </div>
</div>

<style>
  .info-card {
    display: grid;
    grid-template-columns: 1fr 1fr;
    grid-template-rows: 1fr 1fr;
    padding: 30px;
    border: var(--gray-4) solid 1px;
    border-radius: 4px;
    background-color: white;
  }

  .info-card div {
    display: flex;
    flex-direction: column;
  }

  .title {
    color: var(--purple);
    font-style: normal;
    font-weight: 500;
    font-size: medium;
    margin-bottom: 10px;
  }

  .value {
    color: var(--gray-2);
    font-weight: 300;
    margin-bottom: 10px;
  }

  @media (min-width: 320px) and (max-width: 767px) {
    .info-card {
      display: flex;
      align-items: flex-start;
      justify-content: space-between;
    }
  }
</style>
