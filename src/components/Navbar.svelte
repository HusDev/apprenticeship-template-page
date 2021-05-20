<nav>
  <!-- Harbour Space logo -->
  <img id="logo" src="/assets/img/logo.svg" alt="Harbour Space logo" />
  <div class="user-action">
    <div class="apply-now">
      <span>APPLY NOW</span>
    </div>
    <div class="menu">
      <span>MENU</span>
      <img src="/assets/img/icons/menu.svg" alt="Menu" />
    </div>
  </div>
</nav>

<style>
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 30px;
    background-color: var(--dark-purple);
    margin: 0px;
  }

  #logo { 
      width: 170px;
      cursor: pointer;
  }

  .menu {
    display: flex;
    align-items: center;
    justify-content: space-evenly;
    cursor: pointer;
  }

  .menu span { 
    margin: 0 20px;
    color: white;
}
  
  .user-action { 
    display: flex;
    justify-content: center;
    align-items: center;
  }

  .apply-now {
    display: flex;
    align-items: center;
    justify-content: center;
    background-color: var(--green);
    color: white;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: -50px;
    margin-right: 50px;
    cursor: pointer;
    text-align: center;

  }

  .apply-now:hover { 
    transform: scale(1.1);
}

  .apply-now span {
    width: min-content;
  }
</style>
