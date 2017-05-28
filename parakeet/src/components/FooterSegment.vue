<template>
  <div class="ui grid Footer">
    <div class="twelve wide column ui container ">
      <div class="ui section divider"></div>
      <div class="stackable ui four column grid">
        <div class="row">
          <div class="column">
            <h4 class="ui header Footer--title align-left">Jobs at</h4>
            <div class="ui list Footer--list align-left">
              <div class="item">Home</div>
              <div class="item">Jobs</div>
              <div class="item">About</div>
              <div class="item">Department</div>
            </div>
          </div>
          <div class="column">
            <h4 class="ui header Footer--title align-left">Information</h4>
            <div class="ui list Footer--list align-left">
              <div class="item">F.A.Q.</div>
              <div class="item">Application Process</div>
              <div class="item">Privacy Policy</div>
              <div class="item">Contact</div>
            </div>
          </div>
          <div class="column">
            <h4 class="ui header Footer--title align-left">Follow Us</h4>
            <div class="ui two column grid align-left">
            <div class="column">
              <div class="ui list Footer--list">
                <div class="item"><i class="circular small users icon"></i> <div class="content">Newsletter</div></div>
                <div class="item"><i class="circular small instagram icon"></i><div class="content">Instagram</div></div>
                <div class="item"><i class="circular small twitter icon"></i><div class="content">Twitter</div></div>
                <div class="item"><i class="circular small tumblr icon"></i><div class="content">Tumblr</div></div>
                <div class="item"><i class="circular small linkedin icon"></i><div class="content">Linkedin</div></div>
              </div>
            </div>
            <div class="column">
              <div class="ui list Footer--list">
                <div class="item"><i class="circular small facebook f icon"></i> <div class="content">Facebook</div></div>
                <div class="item"><i class="circular small pinterest icon"></i><div class="content">Pinterest</div></div>
                <div class="item"><i class="circular small youtube icon"></i><div class="content">Youtube</div></div>
                <div class="item"><i class="circular small google icon"></i><div class="content">Google</div></div>
              </div>
            </div>
            </div>
          </div>
          <div class="column">
            <h4 class="ui header Footer--title align-left">Job Alert</h4>
            <span class="Footer--subtitle align-left">Subscribe to our job alert</span>
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
  &--title, &--subtitle, &--list, &--item {
    font-family: 'Open Sans', sans-serif;
    font-size: 12px;
    letter-spacing: 0.5px;
  }
  &--subtitle {
    color: #979797;
    font-size: 12px;
    float: left;
  }
  &--list, &--item {
    color: #979797;
  }
}
</style>
