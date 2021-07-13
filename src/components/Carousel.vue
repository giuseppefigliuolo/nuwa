<template>
  <section>
    <div class="tab fixed-tab vertical-text">
      <div class="border border--gray"></div>
      <div class="content">
        <h2 class="text-uppercase">personale richiesto</h2>
        <p class="text-uppercase">fasi di colonizzazione</p>
      </div>
    </div>
    <div class="tab fixed-tab vertical-text">
      <div class="border border--gray"></div>
      <div class="content">
        <h2 class="text-uppercase">personale richiesto</h2>
        <p class="text-uppercase">fasi di colonizzazione</p>
      </div>
    </div>
  </section>
</template>

<script>
export default {}
</script>

<style lang="scss" scoped>
section {
  height: 800px;
  margin-bottom: 6rem;
}

.tab {
  height: 100%;
  display: flex;
  flex-direction: row-reverse;
}

.vertical-text {
  writing-mode: vertical-rl;
  text-orientation: mixed;
  transform: scale(-1);
}

.fixed-tab {
  width: 110px;

  .content {
    height: 70%;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
}

.border {
  margin-bottom: auto;
  height: 48px;
  width: 100%;
  &--gray {
    background: gray;
  }
}
</style>
