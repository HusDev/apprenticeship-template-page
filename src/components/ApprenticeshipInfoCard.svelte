<div class="info-card">
  <div>
    <span class="title">Location</span>
    <span class="value">Bangkok</span>
  </div>
  <div>
    <span class="title">Duration</span>
    <span class="value">1 Year</span>
    <span class="value">Full Time</span>
  </div>
  <div>
    <span class="title">Start Date</span>
    <span class="value">30 June 2020</span>
  </div>
  <div>
    <span class="title">End Date</span>
    <span class="value">3 Aug 2020</span>
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
 