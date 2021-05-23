<script>
  // Cursor event
  let clientX;
  let clientY;
  let myCard;
  let showCursor = false;
  function handleMousemove(e) {
    clientX = e.clientX;
    clientY = e.clientY;
  }

  function handleMouseout() {
    showCursor = false;
  }

  function handleMouseover() {
    showCursor = true;
  }
</script>

<div
  class="testimonial-card"
  bind:this={myCard}
  on:mouseover={handleMouseover}
  on:mouseout={handleMouseout}
  on:mousemove={handleMousemove}
>
  <div class="profile-info">
    <div>
      <img
        class="img-profile"
        src="assets/img/profile-img.svg"
        alt=""
      />
      <div class="description">
        <span class="name">Irene Pereyra</span>
        <span>Interaction Design Fellow ‘19</span>
      </div>
    </div>
    <img src="assets/img/linked-in.svg" alt="" />
  </div>

  <div class="paragraph">
    <p>
      This Fellowship was a turning point in my career. I wouldn’t be where I am
      today without the financial support and experienced offered through the
      program.
    </p>
    <span>Education · B.A. Visual Design</span>
  </div>
</div>

<!-- <div
class={showCursor ? "" : "hide"}
style="left:{clientX}px; top:{clientY - 400}px;"
id="cursor"
>
<span>Drag</span>
</div> -->
<style>
  .testimonial-card {
    border: 1px solid var(--gray-3);
    color: #6a6a6a;
    background-color: white;
    /* cursor: url('./assets/img/cursor.cur') 32 32, default; */
    cursor: url("assets/img/cursor.png"), pointer;
  }

  .paragraph {
    background-color: var(--gray-5);
    padding: 40px 100px;
    font-size: larger;
    font-weight: 300;
  }

  .paragraph span {
    font-size: small;
  }

  .profile-info {
    display: flex;
    justify-content: space-between;
    align-items: center;
  }

  .profile-info {
    padding: 20px;
  }

  .profile-info div {
    display: flex;
    align-items: center;
  }

  .profile-info div .description {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    margin-left: 20px;
  }

  .name {
    color: var(--gray-1);
    font-weight: 500;
  }

  img.img-profile {
    width: 100px;
    height: 100px;
    object-fit: cover;
    border-radius: 50%;
  }

  #cursor {
    position: absolute;
    display: flex;
    justify-content: center;
    align-items: center;
    box-sizing: border-box;
    transition: 0.1s;
    color: white;
    width: 100px;
    height: 50px;
    transform: translate(-50%, -50%);
    border-radius: 30px;
    pointer-events: none;
    background-color: #675dc5ca;
    z-index: 2000;
  }

  #cursor.hide {
    width: 0;
  }

  #cursor.hide span {
    display: none;
  }

  @media (min-width: 320px) and (max-width: 767px) {
    .paragraph {
    background-color: var(--gray-5);
    padding: 40px 20px;
    font-size: larger;
    font-weight: 300;
  }
  }
</style>
