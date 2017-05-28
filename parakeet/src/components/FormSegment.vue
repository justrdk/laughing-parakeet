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
          <vue-form :state="formstate" v-model="formstate" @submit.prevent="onSubmit" class="ui large form">
            <h4 class="ui header Form--information-title align-left">Personal Details*</h4>
            <div class="two fields">
              <div class="field" :class="fieldClassName(formstate.firstname)">
                <validate auto-label class="form-group required-field">
                  <input class="Form--input" v-model ="model.firstname"
                  type="text" name="firstname" placeholder="First Name" required>
                </validate>
              </div>
              <div class="field">
                <div class="field" :class="fieldClassName(formstate.lastname)">
                  <validate auto-label class="form-group required-field">
                    <input class="Form--input" v-model ="model.lastname"
                    type="text" name="lastname" placeholder="Last Name" required>
                  </validate>
                </div>
              </div>
            </div>
            <div class="two fields">
                <div class="field" :class="fieldClassName(formstate.dob)">
                  <validate auto-label class="form-group required-field">
                    <input class="Form--input" v-model="model.dob"
                    type="text" name="dob" placeholder="Date of Birth" required>
                  </validate>
                </div>
                <div class="field" :class="fieldClassName(formstate.email)">
                  <validate auto-label class="form-group required-field">
                    <input class="Form--input" v-model ="model.email"
                    type="email" name="email" placeholder="Email" required>
                  </validate>
              </div>
            </div>
            <div class="two fields">
              <div class="field">
                <div class="three fields">
                  <div class="field" :class="fieldClassName(formstate.address)">
                    <validate auto-label class="form-group required-field Form--label align-left">
                      <label>Address</label>
                      <input class="Form--input" v-model ="model.address"
                      type="text" name="address" placeholder="Address" required>
                    </validate>
                  </div>
                  <div class="field" :class="fieldClassName(formstate.house)">
                    <validate auto-label class="form-group required-field Form--label align-left">
                      <label>Model#</label>
                      <input class="Form--input" v-model ="model.house"
                      type="text" name="house" placeholder="House No." required>
                    </validate>
                  </div>
                  <div class="field" :class="fieldClassName(formstate.zipcode)">
                    <validate auto-label class="form-group required-field Form--label align-left">
                      <label>Zipcode</label>
                      <input class="Form--input" v-model ="model.zipcode"
                      type="number" name="address" placeholder="Zipcode" required>
                    </validate>
                  </div>
                </div>
              </div>
              <div class="field" :class="fieldClassName(formstate.sex)">
                  <validate auto-label class="form-group required-field Form--label align-left">
                    <label>Sex</label>
                    <input class="Form--input" v-model ="model.sex"
                    type="text" name="sex" placeholder="Sex" required>
                  </validate>
              </div>
            </div>
            <div class="two fields">
              <div class="field" :class="fieldClassName(formstate.motivation)">
                <validate auto-label class="form-group required-field Form--label align-left">
                  <label>Your Motivation*</label>
                  <textarea name="motivation" class="Form--textarea"
                  v-model="model.motivation" rows="5" cols="50" required></textarea>
                </validate>
              </div>
              <div class="field">
                <label class="Form--label align-left">Attach your documents (pdf, doc(x), jpg max. 4 Mb)</label>
                <div class="inline fields">
                  <div class="three wide field">
                    <label class="Form--uploadLabel align-left">Resume*</label>
                  </div>
                  <div class="four wide field">
                    <button class="fluid ui button Form--button">
                      <i class="desktop icon"></i> Upload
                      <input type="file" class="Form--upload" />
                    </button>
                  </div>
                </div>
                <div class="inline fields">
                  <div class="three wide field">
                    <label class="Form--uploadLabel align-left">Portfolio</label>
                  </div>
                  <div class="four wide field">
                    <button class="fluid ui button Form--button">
                      <i class="desktop icon"></i> Upload
                      <input type="file" class="Form--upload" />
                    </button>
                  </div>
                </div>
                <div class="inline fields">
                  <div class="three wide field">
                    <label class="Form--uploadLabel align-left">Photo</label>
                  </div>
                  <div class="four wide field">
                    <button class="fluid ui button Form--button">
                      <i class="desktop icon"></i> Upload
                      <input type="file" class="Form--upload" />
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </vue-form> <!--endform-->
        </div> <!-- end container -->
      </div> <!-- end column -->
    </div> <!-- end row -->
  </div>
</template>

<script>
import VueForm from 'vue-form';
import Vue from 'vue';

Vue.use(VueForm);

export default {
  data() {
    return {
      formstate: {},
      model: {
        firstname: '',
        lastname: '',
        email: '',
        dob: '',
        address: '',
        house: '',
        zipcode: '',
        sex: '',
        motivation: '',
      },
    };
  },
  methods: {
    fieldClassName(field) {
      if (!field) {
        return '';
      }
      if ((field.$touched || field.$submitted) && field.$valid) {
        return 'success';
      }
      if ((field.$touched || field.$submitted) && field.$invalid) {
        return 'error';
      }
      return false;
    },
  },
};
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
  &--information-title {
    letter-spacing: 0.6px;
    font-family: 'Open Sans', sans-serif;
    font-size: 14px;
  }
  &--label, &--uploadLabel {
    font-family: 'Open Sans', sans-serif;
    font-weight: bold;
    color: #000000;
    letter-spacing: 0.6px;
  }
  &--label {
    font-size: 14px;
  }
  &--uploadLabel {
    font-size: 12px !important;
  }
  &--input {
    height: 42px;
  }
  &--input, &--textarea {
    background: #ffffff;
    border: none;
    border-radius: 0px !important;
  }
  &--button {
    position: relative;
    overflow: hidden;
    background-color: #005c9d;
    color: #ffffff;
    border: none !important;
    border-radius: 0px;
    font-family: 'Open Sans', sans-serif;
    font-size: 12px;
    font-weight: bold;
    letter-spacing: 0.5px;
  }
  &--upload {
    position: absolute;
    top: 0;
    right: 0;
    margin: 0;
    padding: 0;
    font-size: 20px;
    cursor: pointer;
    opacity: 0;
    filter: alpha(opacity=0);
  }
  .error-field > input {
    border: 2px solid red;
  }
}
</style>
