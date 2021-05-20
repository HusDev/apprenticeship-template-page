<div class="profile">
    <div class="profile-flag">
        <img class="img-profile" src="assets/img/Polina_Nazarova-min.png" alt="" />
        <img class="flag" src="assets/img/flag.svg" alt="">
    </div>
  <div class="description">
    <span class="name">Polina Nazarova</span>
    <span class="job-title">Admission officer</span>
  </div>
</div>

<style>
  .profile {
    display: flex;
    align-items: center;
  }

  .profile .description {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-left: 20px;
    width: 170px;
  }

  span.job-title { 
      color: var(--gray-2);
      font-weight: 300;
  }

  .profile .description .name { 
      color: black;
      font-weight: 500;
  }

  img.img-profile { 
        width: 80px;
        height: 80px;
        object-fit: cover;
        border-radius: 50%;
    }

    img.flag { 
        width: 27px;
        height: 27px;
        object-fit: cover;
        border-radius: 50%;
        display: inline-block;
        margin-left: -25px;
        margin-top: -20px;
    }

</style>
