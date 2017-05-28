<template>
  <div class="ui grid Form">
    <div class="row">
      <div class="sixteen wide column">
        <div class="ui container">
          <h1 class="ui header Form--title align-left">APPLY FOR THE POSITION OF PURCHASING ASSISTANT</h1>
        </div>
      </div>
    </div>
    <div class="row">
      <div class="sixteen wide column">
        <div class="ui container">
          <div class="ui large form">
            <h4 class="ui header Form--information-title align-left">Personal Details*</h4>
            <div class="two fields">
              <div class="field">
                <input class="Form--input" type="text" name="first-name" placeholder="First Name">
              </div>
              <div class="field">
                <input class="Form--input" type="text" name="last-name" placeholder="Last Name">
              </div>
            </div>
            <div class="two fields">
              <div class="field">
                <input class="Form--input" type="text" name="dob" placeholder="Date of Birth">
              </div>
              <div class="field">
                <input class="Form--input" type="email" name="email" placeholder="Email Address">
              </div>
            </div>
            <div class="two fields">
              <div class="field">
                <div class="three fields">
                  <div class="field">
                    <label class="Form--label align-left">Address</label>
                    <input class="Form--input" type="text" name="address" placeholder="Address">
                  </div>
                  <div class="field">
                    <label class="Form--label align-left">House#</label>
                    <input class="Form--input" type="text" name="house" placeholder="House number">
                  </div>
                  <div class="field">
                    <label class="Form--label align-left">Zipcode (Dutch)</label>
                    <input class="Form--input" type="text" name="zipcode" placeholder="Dutch zipcode">
                  </div>
                </div>
              </div>
              <div class="field">
                <label class="Form--label align-left">Sex</label>
                <input class="Form--input" type="text" name="sex" placeholder="Sex">
              </div>
            </div>
            <div class="two fields">
              <div class="field">
                <label class="Form--label align-left">Your Motivation*</label>
                <textarea class="Form--textarea" rows="5" cols="50"></textarea>
              </div>
              <div class="field">
                <label class="Form--label align-left">Attach your documents (pdf, doc(x), jpg max. 4 Mb)</label>
                <div class="inline fields">
                  <div class="three wide field">
                    <label class="Form--label align-left">Resume*</label>
                  </div>
                  <div class="four wide field">
                    <button class="fluid ui button Form--button"><i class="desktop icon"></i> Upload</button>
                  </div>
                </div>
                <div class="inline fields">
                  <div class="three wide field">
                    <label class="Form--label align-left">Portfolio</label>
                  </div>
                  <div class="four wide field">
                    <button class="fluid ui button Form--button"><i class="desktop icon"></i> Upload</button>
                  </div>
                </div>
                <div class="inline fields">
                  <div class="three wide field">
                    <label class="Form--label align-left">Photo</label>
                  </div>
                  <div class="four wide field">
                    <button class="fluid ui button Form--button"><i class="desktop icon"></i> Upload</button>
                  </div>
                </div>
              </div>
            </div>
          </div> <!--endform-->
        </div> <!-- end container -->
      </div> <!-- end column -->
    </div> <!-- end row -->
  </div>
</template>

<script>
</script>

<style lang="scss" scoped>
.Form {
  padding-top: 40px;
  background-color: #f7f7f7;
  &--title {
    letter-spacing: 0.8px;
    font-family: 'Yanone Kaffeesatz', sans-serif;
    font-size: 51px;
  }
  &--information-title{
    letter-spacing: 0.6px;
    font-family: 'Open Sans', sans-serif;
    font-size: 14px;
  }
  &--label {
    font-size: 14px !important;
  }
  &--input {
    height: 42px;
  }
  &--input, &--textarea {
    background: #ffffff;
    border: none !important;
    border-radius: 0px !important;
  }
  &--button {
    background-color: #005c9d;
    color: #ffffff;
    border: none !important;
    border-radius: 0px;
    font-family: 'Open Sans', sans-serif;
    font-size: 12px;
    font-weight: bold;
    letter-spacing: 0.5px;
  }
}
</style>
