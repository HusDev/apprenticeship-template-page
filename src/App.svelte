<script>
  import Navbar from "./components/Navbar.svelte";
  import ScholarshipCard from "./components/ScholarshipCard.svelte";
  import Commitment from "./components/Commitment.svelte";
  import MainButton from "./components/MainButton.svelte";
  import PartnerComponent from "./components/PartnerComponent.svelte";
  import ApplicationDate from "./components/ApplicationDate.svelte";
  import ApprenticeshipInfoCard from "./components/ApprenticeshipInfoCard.svelte";
  import TestimonialCard from "./components/TestimonialCard.svelte";
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
  </div>

  <!-- Section About the apprenticeship -->
  <section class="apprenticeship-info">
    <div class="circle-pattren">
      <img src="/assets/img/profile-2.png" alt="circle pattren" />
    </div>
    <div class="apprenticeship-description">
      <div>
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
  <section>
    <div class="slider">
      <div class="pattern">
        <img
          src="/assets/img/element/background-element-2.svg"
          alt="background element"
        />
      </div>
      <div />
      <TestimonialCard />
    </div>
  </section>

  <div class="container">
    <section class="fqa-section">
      <div class="filter">
        <h1>Frequently asked questions</h1>
        <div class="dropdown">
          <span>Filter by:</span>
          <div>
            <Dropdown />
          </div>
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
  .apprenticeship-info {
    margin-top: 200px;
    display: grid;
    grid-template-columns: 1fr 1fr;
    align-items: center;
    gap: 50px;
    margin: 150px 20%;
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
    margin: 150px 20%;
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
    margin-top: 10px;
  }

  .dropdown span {
    margin-right: 10px;
    margin-top: inherit;
  }

  .fqa-list {
    margin-bottom: 150px;
    border-top: var(--gray-3) solid 1px;
  }

  /* Responsive */

  /* -- Responsive -- */

  /* 
  ##Device = Desktops
  ##Screen = 1281px to higher resolution desktops
*/

  @media (min-width: 1281px) {
    /* Future use */
  }

  /* 
    ##Device = Laptops, Desktops
    ##Screen = B/w 1025px to 1280px
  */

  @media (min-width: 1025px) and (max-width: 1280px) {


    /* First Section Data Science Apprenticeship info */
    .scholarship-info .right-side img {
      left: 0px;
      width: 100%;
    }

    .container {
      padding: 0 5%;
    }

    .apprenticeship-info,
    .calcualtion {
      margin: 150px 5%;
    }

    .scholarship-info div.left-side h1.name {
      font-size: 48px;
    }
    .slider {
      grid-template-columns: 1fr;
      padding: 1px;
      margin: 200px 20%; 
    }

  }

  /* 
    ##Device = Tablets, Ipads (portrait)
    ##Screen = B/w 768px to 1024px
  */

  @media (min-width: 768px) and (max-width: 1024px) {

    .scholarship-info .right-side img {
      left: 0px;
      width: 100%;
    }

    /* First Section Data Science Apprenticeship info */
    .container {
      padding: 0 2%;
    }

    section.apprenticeship-info,
    .calcualtion {
      margin: 150px 2%;
    }

    .scholarship-info div.left-side h1.name {
      font-size: 48px;
    }

    .slider {
      grid-template-columns: 1fr;
      padding: 1px;
      margin: 200px 20px; 
    }
  }

  /* 
    ##Device = Low Resolution Tablets, Mobiles (Landscape)
    ##Screen = B/w 481px to 767px
  */

  @media (min-width: 320px) and (max-width: 767px) {

    /* First Section Data Science Apprenticeship info */
    .container {
      padding: 0 5%;
    }

    .calcualtion {
      margin: 150px 5%;
    }

    section.apprenticeship-info {
      margin: 250px 0 0 0;
    }

    section.scholarship-info {
      grid-template-columns: 1fr;
    }

    .scholarship-info div.left-side h1.name {
      font-size: 32px;
    }

    .scholarship-info .right-side img {
      left: 0px;
      width: 100%;
    }

    section.apprenticeship-info {
      grid-template-columns: 1fr;
      justify-items: center;
    }

    section.apprenticeship-info img {
      z-index: 1;
    }

    section.apprenticeship-info img {
      width: 80%;
      content: url(/assets/img/barcelona.png);
    }

    .apprenticeship-description {
      background-color: var(--purple);
      margin-top: -200px;
      height: 400px;
      margin-bottom: 300px;
    }

    .apprenticeship-description div {
      background-color: white;
      margin: 0 20px;
      padding: 150px 0 0 20px;
      border: var(--gray-3) solid 1px;
      height: 400px;
    }

    .calcualtion {
      display: flex;
      flex-direction: column;
      margin: 0 5%;
    }

    .filter {
      flex-direction: column;
      padding: 10%;
    }

    .filter .dropdown {
      flex-direction: column;
      width: 100%;
      justify-content: stretch;
      align-items: stretch;
      z-index: 2;
    }
    .dropdown div {
      width: 100%;
      margin: 10px 0;
      background-color: white;
      z-index: 2;
    }

    .fqa-list {
      margin-top: 20px;
      border-top: 0;
    }

    .slider {
      grid-template-columns: 1fr;
      padding: 1px;
      margin: 200px 20px; 
    }

    .name-element img{
      display: none;
    }
  }
</style>
