<template>
  <div class="ui grid top-segment no-padding">
    <div class="sixteen wide column">
      <div class="ui container">
        <div class="ui raised segment title-segment">
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
.top-segment {
  display: flex;
  align-items: center;
  justify-content: center;
  height: 305px;
  background-image: url('../assets/top-image.jpg');
  .title-segment {
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
