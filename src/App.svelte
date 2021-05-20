<script>
  import Navbar from "./components/Navbar.svelte";
  import ScholarshipCard from "./components/ScholarshipCard.svelte";
  import Commitment from "./components/Commitment.svelte";
  import MainButton from "./components/MainButton.svelte";
  import PartnerComponent from "./components/PartnerComponent.svelte";
  import ApplicationDate from "./components/ApplicationDate.svelte";
  import ApprenticeshipInfoCard from "./components/ApprenticeshipInfoCard.svelte";
  import TestimonialCard from "./components/TestimonialCard.svelte";
  import DropDownFilter from "./components/DropDownFilter.svelte";
  import FrequentQuestion from "./components/FrequentQuestion.svelte";
import Dropdown from "./components/Dropdown.svelte";
</script>

<main>
  <Navbar />
  <div class="container">
    <!-- Section Data Science Apprenticeship info -->
    <section class="scholarship-info">
      <div class="left-side">
        <div class="name-element">
          <h1 class="name">Interaction Design Apprenticeship</h1>
          <img
            src="/assets/img/element/background-element-1.svg"
            alt="background element"
          />
        </div>
        <span class="slogan">
          A fully funded work-study program to launch your tech career
        </span>
        <span>
          Harbour.Space has partnered with SCG to empower driven talent and
          eliminate the barriers to accessing exceptional education and career
          opportunities through a Masters Fellowship.
        </span>
        <span><b>Position: </b> Marketing Performance</span>
        <MainButton />
      </div>
      <div class="right-side">
        <!-- Powered By -->
        <PartnerComponent />
        <!-- Application expiration date -->
        <ApplicationDate />
        <!-- programme date-location info -->
        <div class="date-location">
          <ApprenticeshipInfoCard />
          <img
            src="/assets/img/element/background-element-2.svg"
            alt="background element"
          />
        </div>
      </div>
    </section>

    <!-- Section About the apprenticeship -->
    <section class="apprenticeship-info">
      <div class="circle-pattren">
        <img src="/assets/img/profile-2.png" alt="circle pattren" />
      </div>
      <div class="apprenticeship-description">
        <span class="title">About the apprenticeship</span>
        <p>
          Our Apprenticeship opportunities are designed to give talented and
          driven young people from any background access to top-class education,
          development opportunities and network. This offer includes a
          scholarship for a 12 month Master’s degree in Data Science and work
          experience in an exciting technology company with the possibility of a
          job upon graduation.
        </p>
      </div>
    </section>

    <!-- Section Calculation -->
    <section class="calcualtion">
      <!-- Grid -->
      <div class="scholarship-value">
        <ScholarshipCard />
      </div>
      <div class="study-commitment">
        <Commitment />
      </div>
      <div class="work-commitment">
        <Commitment />
      </div>
      <!-- -- Graduation line --  -->
      <div class="graduation-line">
        <div class="line" />
        <span>Graduation</span>
        <div class="line" />
      </div>
      <div class="contract">
        <Commitment />
      </div>
    </section>
  </div>

  <section>
    <div class="slider">
      <div class="pattern">
        <img
          src="/assets/img/element/background-element-2.svg"
          alt="background element"
        />
      </div>
      <TestimonialCard />
      <TestimonialCard />
      <TestimonialCard />
    </div>
  </section>

  <div class="container">
    <section class="fqa-section">
      <div class="filter">
        <h1>Frequently asked questions</h1>
        <div class="dropdown">
          <span>Filter by:</span>
          <Dropdown/>
        </div>
      </div>
      <div class="fqa-list">
        <FrequentQuestion />
        <FrequentQuestion />
        <FrequentQuestion />
        <FrequentQuestion />
      </div>
    </section>
  </div>
</main>

<style>
  .container {
    padding: 0 20%;
    margin: auto;
  }

  /* --- First Section CSS --- */
  span {
    color: var(--gray-2);
    font-weight: 300;
  }

  .name-element {
    position: relative;
  }

  .name-element img {
    z-index: -1;
    position: absolute;
    right: -70px;
    top: -70px;
    width: 250px;
  }

  section.scholarship-info {
    display: grid;
    grid-template-columns: 1fr 1fr;
    gap: 100px;
    margin-top: 100px;
    margin-bottom: 50px;
  }

  .scholarship-info .left-side {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
  }

  .scholarship-info .right-side {
    display: grid;
    margin-bottom: 30px;
    grid-row-gap: 25px;
  }

  .scholarship-info .right-side .date-location {
    position: relative;
  }

  .scholarship-info .right-side img {
    position: absolute;
    top: 50px;
    left: 50px;
    z-index: -1;
  }

  .scholarship-info div span {
    font-weight: 300;
    font-size: 22px;
    margin-bottom: 20px;
  }

  .scholarship-info div .slogan {
    font-weight: 500;
    color: var(--gray-1);
  }

  .scholarship-info div .name {
    font-size: 48px;
    color: var(--purple);
    font-weight: 500;
  }

  /* --- End First Section CSS --- */

  /* --- Second Section CSS --- */
  section.apprenticeship-info {
    margin-top: 200px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 50px;
  }

  .circle-pattren {
    display: flex;
    width: 400px;
    height: 400px;
    align-items: center;
    justify-content: center;
    background-image: url("/assets/img/Pattern.png");
    background-repeat: no-repeat;
    box-sizing: border-box;
    background-position: center;
    background-size: cover;
  }

  .circle-pattren img {
    border-radius: 50%;
    width: 90%;
  }

  .apprenticeship-description .title {
    font-weight: 500;
    font-size: 48px;
    color: var(--purple);
  }
  /* --- End Second Section CSS --- */

  /* Third Section  */
  .calcualtion {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 30px;
    margin: 150px 0;
  }

  .calcualtion .scholarship-value {
    display: flex;
    grid-column: 1/2;
    grid-row: 1/4;
  }
  .calcualtion .study-commitment {
    grid-column: 2/3;
    grid-row: 1 / 2;
  }
  .calcualtion .work-commitment {
    grid-column: 3 / 4;
    grid-row: 1 / 2;
  }
  .calcualtion .graduation-line {
    grid-column: 2/4;
    grid-row: 2/3;
    display: grid;
    grid-template-columns: 2fr 1fr 2fr;
    align-items: center;
    justify-content: center;
  }

  .calcualtion .graduation-line span {
    text-align: center;
    font-weight: 500;
    font-size: 16px;
  }

  .calcualtion .graduation-line .line {
    border-bottom: var(--gray-3) solid 1px;
  }

  .calcualtion .contract {
    grid-column: 2/4;
    grid-row: 3/4;
  }

  /* End Third Section  */

  /* Forth Section */
  .slider {
    position: relative;
    display: grid;
    grid-template-columns: 1fr 1fr 1fr;
    gap: 20px;
    margin-top: 300px;
  }

  .slider .pattern {
    position: absolute;
    z-index: -1;
    margin: auto;
    position: absolute;
    text-align: center;
    width: 100%;
    height: 100%;
    top: 0;
    left: 0;
    bottom: 0;
    right: 0;
  }

  .slider .pattern img { 
    width: 50%;
    margin-top: -100px;
  }

  .fqa-section {
    margin-top: 200px;
  }

  .filter {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    height: 200px;
  }

  .filter h1 {
    font-size: 48px;
    color: var(--purple);
    font-weight: 500;
    width: 400px;
    margin: 0;
  }

  .dropdown {
    display: flex;
    justify-content: space-between;
    align-items: flex-start;
    margin-top: 10px
  }

  .dropdown span {
    margin-right: 10px;
    margin-top: inherit;
  }

  .fqa-list {
    margin-bottom: 150px;
    border-top: var(--gray-3) solid 1px;
  }
</style>
