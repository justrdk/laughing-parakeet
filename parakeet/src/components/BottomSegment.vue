<template>
  <div class="stackable ui grid Bottom-Segment">
    <div class="fourteen wide column">
      <div class="ui container">
        <div class="ui raised segment Bottom-Segment--title">
          <div class="ui two column grid">
            <div class="column Bottom-Segment--column">
              <h1 class="ui header align-left">Application Procedure</h1>
              <ul class="ui bulleted list Bottom-Segment--list">
                <div class="item">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod.</div>
                <div class="item">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod.</div>
                <div class="item">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod.</div>
                <div class="item">Lorem ipsum dolor sit amet, consectetur adipisicing elit, sed do eiusmod.</div>
              </ul>
            </div>
            <div class="column Bottom-Segment--column">
              <h1 class="ui header align-left">Got a Question</h1>
              <h4 class="ui header align-left">Please contact recruitment</h4>
              <span class="Bottom-Segment--metadata">T. +31 20 123 456 78</span>
              <br/>
              <span class="Bottom-Segment--metadata">or <a class="Bottom-Segment--link">send us an email</a></span>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'bottom-segment',
};
</script>

<style lang="scss" scoped>
.Bottom-Segment {
  display: flex;
  align-items: center;
  justify-content: center;
  background-image: url('../assets/top-image.jpg');
  &--column {
    padding: 40px !important;
  }
  &--title {
    background-color: #ffffff;
    h1.header {
      letter-spacing: 0.6px;
      font-family: 'Yanone Kaffeesatz', sans-serif;
      font-size: 41px;
    }
    h4.header {
      letter-spacing: 0.6px;
      font-family: 'Yanone Kaffeesatz', sans-serif;
      font-size: 14px;
    }
  }
  &--list {
    font-size: 12px;
    font-family: 'Open Sans', sans-serif;
    letter-spacing: 0.5px;
    color: #4a4a4a;
  }
  &--metadata, &--link {
    font-size: 12px;
    letter-spacing: 0.5px;
    color: #a8a8a8;
    font-family: 'Open Sans', sans-serif;
    float: left;
  }
  &--metadata {
    font-weight: bold;
  }
  &--link {
    padding-left: 5px;
    text-decoration: underline;
    font-weight: normal;
    float: right;
  }
}
</style>
