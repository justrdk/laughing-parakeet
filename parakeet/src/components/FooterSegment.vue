<template>
  <div class="ui grid Footer">
    <div class="twelve wide column ui container ">
      <div class="ui section divider"></div>
      <div class="stackable ui four column grid">
        <div class="row">
          <div class="column">
            <h4 class="ui header Footer--title">Jobs at</h4>
            <div class="ui list Footer--list">
              <div class="item">Home</div>
              <div class="item">Jobs</div>
              <div class="item">About</div>
              <div class="item">Department</div>
            </div>
          </div>
          <div class="column">
            <h4 class="ui header Footer--title">Information</h4>
            <div class="ui list Footer--list">
              <div class="item">F.A.Q.</div>
              <div class="item">Application Process</div>
              <div class="item">Privacy Policy</div>
              <div class="item">Contact</div>
            </div>
          </div>
          <div class="column">
            <h4 class="ui header Footer--title">Follow Us</h4>
            <div class="ui list Footer--list">
              <div class="item"><i class="users icon"></i> <div class="content">Newsletter</div></div>
              <div class="item"><i class="users icon"></i><div class="content">Instagram</div></div>
              <div class="item"><i class="users icon"></i><div class="content">Twitter</div></div>
              <div class="item"><i class="users icon"></i><div class="content">Tumblr</div></div>
              <div class="item"><i class="users icon"></i><div class="content">Linkedin</div></div>
            </div>
          </div>
          <div class="column">
            <h4 class="ui header Footer--title">Job Alert</h4>
            <span class="Footer--item">Subscribe to our job alert</span>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: 'footer-segment',
};
</script>
<style lang="scss" scoped>
.Footer {
  &--title {
    font-family: 'Open Sans', sans-serif !important;
    font-size: 12px;
    letter-spacing: 0.5px;
  }
  &--list, &--item {
    font-size: 12px;
    font-family: 'Open Sans', sans-serif;
    letter-spacing: 0.5px;
    color: #979797;
  }
}
</style>
