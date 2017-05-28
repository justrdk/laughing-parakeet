<template>
  <div class="stackable ui grid Image-Segment no-padding">
    <div class="fourteen wide column">
      <div class="ui container">
        <div class="ui raised segment Image-Segment--title">
          <h1 class="ui header white-text">PURCHASING ASSISTANT</h1>
          <h2 class="ui header white-text">AMSTERDAM, THE NETHERLANDS</h2>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'top-segment',
};
</script>

<style lang="scss" scoped>
.Image-Segment {
  display: flex;
  align-items: center;
  justify-content: center;
  background-image: url('../assets/top-image.jpg');
  min-height: 305px;
  &--title {
    min-height: 174px;
    background-color: rgba(0, 0, 0, 0.37);
    h1.header {
      letter-spacing: 1.1px;
      font-family: 'Yanone Kaffeesatz', sans-serif;
      font-size: 72px;
    }
    h2.header {
      letter-spacing: 1.1px;
      font-family: 'Yanone Kaffeesatz', sans-serif;
      font-size: 42px
    }
  }
}
</style>
