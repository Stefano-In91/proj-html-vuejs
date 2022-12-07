<script>
export default {
  name: "DiscountCards",
};
</script>

<template>
  <div id="promos" class="column-between text-center">
    <div class="discount-card">
      <div>
        <a><i class="fa-solid fa-images"></i></a>
        <a><p>Demos</p></a>
      </div>
    </div>
    <div class="discount-card">
      <div>
        <a
          ><p class="discount"><small>$</small>39</p></a
        >
        <a><p>On Sale</p></a>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
#promos {
  position: fixed;
  z-index: 3;
  top: 15%;
  right: 0;
  cursor: pointer;
  .discount-card {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    background-color: var(--lightbg-color);
    height: 70px;
    width: 70px;
    border-radius: 8px;
    font-size: 1rem;
    &:first-of-type {
      margin-bottom: 0.5rem;
    }
    i {
      font-size: 2rem;
      margin-bottom: 0.5rem;
    }
    p {
      color: rgb(1, 1, 84);
      font-size: 1rem;
      margin: 0;
      &.discount {
        color: rgb(1, 106, 1);
        font-size: 1.5rem;
        margin-bottom: 0.5rem;
        small {
          vertical-align: top;
        }
      }
    }
  }
}
</style>
