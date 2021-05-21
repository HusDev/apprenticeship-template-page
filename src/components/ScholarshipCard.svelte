<script>
  export let total_value;
  export let tuition;
  export let remaining;
  export let stipend_per_year;
  export let stipend_per_month;
</script>
<div class="card">
  <div class="title-fee">
    <span class="title value">Scholarship value</span>
    <span class="fee">€{total_value.toLocaleString()}</span>
  </div>

  <div class="line" />
  <div class="details">
    <div>
      <span class="title">Tuition covered</span>
      <span>€{tuition.toLocaleString()}</span>
    </div>
    <div>
      <span class="title">Remaining</span>
      <span>€{remaining.toLocaleString()}</span>
    </div>
    <div class="col-2-span">
      <span class="title">Living stipend</span>
      <span>€{stipend_per_year.toLocaleString()} (€{stipend_per_month.toLocaleString()}/month)</span>
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

  .title-fee {
    display: flex;
    flex-direction: column;
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
    color: var(--gray-1);
  }

  .col-2-span { 
    grid-column: 1/3;
    grid-row: 2/3;
  }
  .value {
    display: inline-block;
    margin-bottom: 20px;
  }
  @media (min-width: 1025px) and (max-width: 1280px) {
    .value,
    .fee {
      margin: 0;
    }
  }
  @media (min-width: 320px) and (max-width: 767px) {
    .line {
      visibility: hidden;
    }
    .card {
      display: grid;
      grid-template-columns: 1fr;
      border: 0;
    }

    .value,
    .fee {
      margin: 0;
    }

    .card div {
      display: flex;
      flex-direction: column;
    }

    .card div.details {
      display: grid;
      grid-template-columns: 1fr 1fr;
    }

    .card div {
      margin-bottom: 10px;
    }
  }
</style>
