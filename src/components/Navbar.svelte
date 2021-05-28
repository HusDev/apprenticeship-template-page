<script lang="ts">
import HamburgerManu from "./HamburgerManu.svelte";
</script>
<nav>
  <!-- Harbour Space logo -->
  <img id="logo" src="/assets/img/logo.svg" alt="Harbour Space logo" />
  <div class="user-action">
    <div class="apply-now">
      <span>APPLY NOW</span>
    </div>
    <div class="menu">
      <span>MENU</span>
      <HamburgerManu/>
    </div>
  </div>
</nav>

<style>
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 20px 30px;
    background-color: var(--dark-purple);
    margin: 0px;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 10;
    padding-right: 50px;
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
    position: absolute;
    align-items: center;
    justify-content: center;
    background-color: var(--green);
    color: white;
    width: 100px;
    height: 100px;
    border-radius: 50%;
    margin-bottom: -50px;
    margin-right: 250px;
    cursor: pointer;
    text-align: center;
    transition: 200ms cubic-bezier(0.455, 0.03, 0.515, 0.955) 0s;
  }

  .apply-now:hover { 
    padding: 5px;
  }

  .apply-now span {
    width: min-content;
  }


  /* 
    ##Device = Low Resolution Tablets, Mobiles (Landscape)
    ##Screen = B/w 481px to 767px
  */
  
  @media (min-width: 320px) and (max-width: 767px) {
    nav .apply-now {
      visibility: hidden;
    }
  }
  
</style>
