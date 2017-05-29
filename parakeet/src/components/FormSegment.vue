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
            <h4 class="ui header Form--information-title align-left">Personal Details* {{model.dob}}</h4>
            <div class="two fields">
              <div class="field" :class="fieldClassName(formstate.firstname)">
                <validate auto-label class="form-group required-field">
                  <div class="ui icon input">
                    <i class="checkmark icon"
                    v-show="formstate.firstname && (formstate.firstname.$dirty || formstate.firstname.$touched || formstate.firstname.$submitted) && formstate.firstname.$valid"></i>
                    <input class="Form--input" :class="fieldClassName(formstate.firstname)" v-model ="model.firstname"
                    type="text" name="firstname" placeholder="First Name" required>
                  </div>
                </validate>
              </div>
              <div class="field">
                <div class="field" :class="fieldClassName(formstate.lastname)">
                  <validate auto-label class="form-group required-field">
                    <div class="ui icon input">
                      <i class="checkmark icon"
                      v-show="formstate.lastname && (formstate.lastname.$dirty || formstate.lastname.$touched || formstate.lastname.$submitted) && formstate.lastname.$valid"></i>
                      <input class="Form--input" :class="fieldClassName(formstate.lastname)" v-model ="model.lastname"
                      type="text" name="lastname" placeholder="Last Name" required>
                    </div>
                  </validate>
                </div>
              </div>
            </div>
            <div class="two fields">
                <div class="field" :class="fieldClassName(formstate.dob)">
                  <validate auto-label class="form-group required-field">
                    <div class="ui calendar" id="dobcalendar">
                      <div class="ui icon input">
                        <i class="checkmark icon"
                        v-show="formstate.dob && (formstate.dob.$dirty || formstate.dob.$touched || formstate.dob.$submitted) && formstate.dob.$valid"></i>
                        <input class="Form--input" :class="fieldClassName(formstate.dob)" v-model ="model.dob"
                        type="text" name="dob" placeholder="Date of birth" required>
                      </div>
                    </div>
                  </validate>
                </div>
                <div class="field" :class="fieldClassName(formstate.email)">
                  <validate auto-label class="form-group required-field">
                    <div class="ui icon input">
                      <i class="checkmark icon"
                      v-show="formstate.email && (formstate.email.$dirty || formstate.email.$touched || formstate.email.$submitted) && formstate.email.$valid"></i>
                      <input class="Form--input" :class="fieldClassName(formstate.email)" v-model ="model.email"
                      type="email" name="email" placeholder="Email" required>
                    </div>
                  </validate>
              </div>
            </div>
            <div class="two fields">
              <div class="field">
                <div class="three fields">
                  <div class="field" :class="fieldClassName(formstate.address)">
                    <validate auto-label class="form-group required-field Form--label align-left">
                      <label>Address</label>
                      <div class="ui icon input">
                        <i class="checkmark icon"
                        v-show="formstate.address && (formstate.address.$dirty || formstate.address.$touched || formstate.address.$submitted) && formstate.address.$valid"></i>
                        <input class="Form--input" :class="fieldClassName(formstate.address)" v-model ="model.address"
                        type="text" name="address" placeholder="Address" required>
                      </div>
                    </validate>
                  </div>
                  <div class="field" :class="fieldClassName(formstate.house)">
                    <validate auto-label class="form-group required-field Form--label align-left">
                      <label>Model#</label>
                      <div class="ui icon input">
                        <i class="checkmark icon"
                        v-show="formstate.house && (formstate.house.$dirty || formstate.house.$touched || formstate.house.$submitted) && formstate.house.$valid"></i>
                        <input class="Form--input" :class="fieldClassName(formstate.house)" v-model ="model.house"
                        type="number" name="house" placeholder="House No" required>
                      </div>
                    </validate>
                  </div>
                  <div class="field" :class="fieldClassName(formstate.zipcode)">
                    <validate auto-label class="form-group required-field Form--label align-left">
                      <label>Zipcode</label>
                      <div class="ui icon input">
                        <i class="checkmark icon"
                        v-show="formstate.zipcode && (formstate.zipcode.$dirty || formstate.zipcode.$touched || formstate.zipcode.$submitted) && formstate.zipcode.$valid"></i>
                        <input class="Form--input" :class="fieldClassName(formstate.zipcode)" v-model ="model.zipcode"
                        type="number" name="zipcode" placeholder="Zipcode" required>
                      </div>
                    </validate>
                  </div>
                </div>
              </div>
              <div class="field" :class="fieldClassName(formstate.sex)">
                  <validate auto-label class="form-group required-field Form--label align-left">
                    <label>Sex</label>
                     <div class="ui icon input">
                      <i class="checkmark icon"
                      v-show="formstate.sex && (formstate.sex.$dirty || formstate.sex.$touched || formstate.sex.$submitted) && formstate.sex.$valid"></i>
                      <input class="Form--input" :class="fieldClassName(formstate.sex)" v-model ="model.sex"
                      type="text" name="sex" placeholder="Sex" required>
                    </div>
                  </validate>
              </div>
            </div>
            <div class="two fields">
              <div class="field" :class="fieldClassName(formstate.motivation)">
                <validate auto-label class="form-group required-field Form--label align-left">
                  <label>Your Motivation*</label>
                   <div class="ui icon input">
                      <i class="checkmark icon"
                      v-show="formstate.motivation && (formstate.motivation.$dirty || formstate.motivation.$touched || formstate.motivation.$submitted) && formstate.motivation.$valid"></i>
                      <textarea name="motivation" class="Form--textarea" :class="fieldClassName(formstate.motivation)"
                        v-model="model.motivation" rows="6" cols="50" required>
                      </textarea>
                    </div>
                </validate>
              </div>
              <div class="field">
                <label class="Form--label align-left">Attach your documents (pdf, doc(x), rtf, txt, jpg, png, max. 4 Mb)</label>
                <div class="inline fields">
                  <div class="four wide field">
                    <label class="Form--uploadLabel align-left">Resume*</label>
                     <i class="checkmark icon"
                      v-show="validResume === true"></i>
                  </div>
                  <div class="eight wide field">
                    <button class="fluid ui button Form--button">
                      <i class="desktop icon"></i> Upload
                      <input type="file" class="Form--upload" @change="resumeChange" />
                    </button>
                    <span class="upload-error" v-show="resumeError !== ''">{{resumeError}}</span>
                  </div>
                </div>
                <div class="inline fields">
                  <div class="four wide field">
                    <label class="Form--uploadLabel align-left">Portfolio</label>
                    <i class="checkmark icon"
                      v-show="validPortfolio === true"></i>
                  </div>
                  <div class="eight wide field">
                    <button class="fluid ui button Form--button">
                      <i class="desktop icon"></i> Upload
                      <input type="file" class="Form--upload" @change="portfolioChange" />
                    </button>
                    <span class="upload-error" v-show="portfolioError !== ''">{{portfolioError}}</span>
                  </div>
                </div>
                <div class="inline fields">
                  <div class="four wide field">
                    <label class="Form--uploadLabel align-left">Photo</label>
                    <i class="checkmark icon"
                      v-show="validPhoto === true"></i>
                  </div>
                  <div class="eight wide field">
                    <button class="ui fluid button Form--button">
                      <i class="desktop icon"></i> Upload
                      <input type="file" class="Form--upload" @change="photoChange" />
                    </button>
                    <span class="upload-error" v-show="photoError !== ''">{{photoError}}</span>
                  </div>
                </div>
                <div class="inline fields">
                  <div class="four wide field">
                    <div class="ui checkbox">
                      <input type="checkbox" name="example">
                      <label id="submitLabel" class="Form--submitLabel align-left">Send me a copy</label>
                    </div>
                  </div>
                  <div class="eight wide field">
                    <button class="fluid ui button Form--button" type="submit">
                      Apply for this job
                    </button>
                  </div>
                </div>
              </div>
            </div>
          </vue-form> <!--endform-->
        </div> <!-- end container -->
      </div> <!-- end column -->
    </div> <!-- end row -->
    <confirmation-modal></confirmation-modal>
  </div>
</template>

<script>
import VueForm from 'vue-form';
import Vue from 'vue';
import ConfirmationModal from './ConfirmationModal';

const FILE_SIZE = 4194304;
const UPLOAD_ERROR = 'Invalid file type or size';
Vue.use(VueForm);

export default {
  mounted() {
    const today = new Date();
    $('#dobcalendar').calendar({
      type: 'date',
      maxDate: new Date(today.getFullYear(), today.getMonth(), today.getDate()),
      onChange: (date, text) => {
        this.model.dob = text;
      },
    });
  },
  components: {
    ConfirmationModal,
  },
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
        resume: '',
        portfolio: '',
        photo: '',
      },
      validResume: false,
      validPortfolio: false,
      validPhoto: false,
      validFileSize: 4000,
      resumeError: '',
      portfolioError: '',
      photoError: '',
    };
  },
  methods: {
    fieldClassName(field) {
      if (!field) {
        return '';
      }
      if ((field.$dirty || field.$touched || field.$submitted) && field.$valid) {
        return 'success';
      }
      if ((field.$dirty || field.$touched || field.$submitted) && field.$invalid) {
        return 'error';
      }
      return false;
    },
    validPhotoType(type) {
      switch (type) {
        case 'jpeg':
        case 'png':
          return true;
        default:
          return false;
      }
    },
    validFileType(type) {
      switch (type) {
        case 'pdf':
        case 'rtf':
        case 'docx':
        case 'txt':
          return true;
        default:
          return false;
      }
    },
    resumeChange(e) {
      if (e.target.files.length === 1) {
        const file = e.target.files[0];
        const { name, type, size } = file;
        this.resume = name;
        const fileType = type.split('/')[1];
        this.validResume = this.validFileType(fileType) && size < FILE_SIZE;
        this.resumeError = !this.validResume ? 'Invalid file type or size' : '';
      } else {
        this.resumeError = 'Invalid file type or size';
        this.validResume = false;
      }
    },
    portfolioChange(e) {
      if (e.target.files.length === 1) {
        const file = e.target.files[0];
        const { name, type, size } = file;
        this.resume = name;
        const fileType = type.split('/')[1];
        this.validPortfolio = this.validFileType(fileType) && size < FILE_SIZE;
        this.portfolioError = !this.validPortfolio ? 'Invalid file type or size' : '';
      } else {
        this.portfolioError = 'Invalid file type or size';
        this.validPortfolio = false;
      }
    },
    photoChange(e) {
      if (e.target.files.length === 1) {
        const file = e.target.files[0];
        const { name, type, size } = file;
        this.resume = name;
        const fileType = type.split('/')[1];
        this.validPhoto = this.validPhotoType(fileType) && size < FILE_SIZE;
        this.photoError = !this.validPhoto ? UPLOAD_ERROR : '';
      } else {
        this.photoError = UPLOAD_ERROR;
        this.validPhoto = false;
      }
    },
    onSubmit() {
      if (this.formstate.$valid && this.validPortfolio && this.validResume && this.validPhoto) {
        $('.Confirmation')
          .modal({
            closable: false,
            blurring: true,
          })
          .modal('show');
      }
      if (!this.validPortfolio) {
        this.portfolioError = UPLOAD_ERROR;
      }
      if (!this.validResume) {
        this.resumeError = UPLOAD_ERROR;
      }
      if (!this.validPhoto) {
        this.photoError = UPLOAD_ERROR;
      }
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
  #submitLabel {
    color: #979797;
    font-size: 12px;
    font-weight: bold;
    font-family: 'Open Sans', sans-serif;
    letter-spacing: 0.5px;
  }
  &--input {
    height: 42px;
    font-weight: bold;
    font-family: 'Open Sans', sans-serif;
    font-size: 12px !important;
    border: none !important;
  }
  input.success {
    color: #01385f !important;
    border: none !important;
  }
  input.error {
    border: solid 1px #c80000 !important;
  }
  i.checkmark.icon {
    color: #01385f;
    font-size: 12px;
    font-weight: bold;
  }
  &--input, &--textarea {
    background: #ffffff;
    border: none;
    border-radius: 0px !important;
  }
  &--button {
    position: relative;
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
  .upload-error {
    font-size: 12px;
    color: #c80000;
    font-weight: bold;
    font-family: 'Open Sans', sans-serif;
  }
}
</style>
