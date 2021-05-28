<script lang="ts">
  export let isMore: boolean = false;
  let rotate: boolean = false;
  const clickHandle = () => {
    // add class to rotate plus icon
    if (isMore) {
      isMore = !isMore;
    } else {
      setTimeout(() => {
        rotate = true;
        setTimeout(() => {
          isMore = !isMore;
          rotate = false;
        }, 300);
      }, 50);
    }
  }
</script>

<div class="read-more {isMore ? 'more' : ''}" on:click={clickHandle}>
  <div
    class="plus-minus {isMore ? 'rotate' : ''} {rotate ? 'first-rotate' : ''}"
  >
    <span class="horizontal-bar" />
    <span class="vertical-bar" />
  </div>
</div>

<style>
  .read-more {
    display: flex;
    justify-content: center;
    align-items: center;
    color: #959595;
    width: 48px;
    height: 48px;
    border-radius: 50%;
    border: #959595 solid 1px;
    cursor: pointer;
    transition: 100ms;
  }

  .more {
    border: var(--purple) solid 25px;
    width: 0;
    height: 0;
  }

  .plus-minus {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    transition: 300ms;
  }

  .plus-minus span {
    width: 2px;
    height: 14px;
    border-radius: 4px;
    background-color: grey;
  }

  .plus-minus.rotate {
    transform-origin: center;
    transform: rotate(720deg);
    color: white;
  }

  .plus-minus.rotate span {
    background-color: rgb(255, 255, 255);
  }

  .plus-minus.rotate .vertical-bar {
    visibility: hidden;
  }

  .plus-minus .horizontal-bar {
    transform-origin: center;
    transform: translateY(7px) rotate(90deg);
  }
  .plus-minus .vertical-bar {
    transform: translateY(-7px);
  }

  .first-rotate {
    transform: rotate(360deg);
  }

  .first-rotate span {
    background-color: var(--purple);
  }
</style>
