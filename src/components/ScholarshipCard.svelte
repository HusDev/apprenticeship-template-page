<div class="card">
    <div>
        <span class="title value">Scholarship value</span>
        <span class="fee">€31,300</span>
    </div>

  <div class="line" />
  <div class="details">
    <div>
      <span class="title">Tuition covered</span>
      <span>€20,900</span>
    </div>
    <div>
      <span class="title">Remaining</span>
      <span>€2,000</span>
    </div>
    <div>
      <span class="title">Living stipend</span>
      <span>€8,400 (€700/month)</span>
    </div>
  </div>
</div>

<style>
  span {
    color: var(--gray-2);
    font-weight: 300;
  }

  .card {
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    padding: 20px;
    border: var(--gray-3) solid 1px;
  }

  .line {
    border-bottom: var(--gray-3) solid 1px;
    margin: 10px;
    margin-bottom: -80px;
  }

  .details {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 20px;
  }

  .details div {
    display: flex;
    flex-direction: column;
  }

  .details div span {
    margin-bottom: 10px;
  }

  .title {
    color: var(--purple);
    font-weight: 500;
  }
  .fee {
    font-weight: 300;
    font-size: 48px;
    margin-top: 40px;
  }

  .value { 
      display: inline-block;
      margin-bottom: 20px;
  }
</style>
