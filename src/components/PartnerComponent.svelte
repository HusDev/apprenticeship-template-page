<script lang="ts">
  export let image: string;
  export let name: string;
</script>

<div class="partner">
  <img src={image} alt="partner logo" />

  <div>
    <span>Powered by:</span>
    <span class="name">{name}</span>
  </div>
</div>

<style>
  .partner {
    display: flex;
    align-items: center;
  }

  .partner div {
    display: flex;
    flex-direction: column;
  }

  span {
    color: var(--gray-2);
    margin-bottom: 10px;
    margin-left: 20px;
    font-weight: 300;
  }

  .name {
    font-size: 27px;
    font-weight: 300;
    color: var(--gray-2);
  }

  img {
    width: 150px;
  }
</style>
