<template>
<div class="ui basic small modal Confirmation">
  <div class="ui icon header Confirmation--title">
     <i class="checkmark icon green"></i>
    Successful Submission
  </div>
  <div class="content">
   <p>Thanks for submitting your information. Will make sure we contact you as soon as possible!</p>
  </div>
  <div class="actions">
    <div class="ui green ok inverted button">
      <i class="checkmark icon"></i> ok
    </div>
  </div>
</div>
</template>
<script>
  export default {
    name: 'confirmation-modal',
  };
</script>
<style lang="scss" scoped>
.Confirmation {
  &--title {
    text-align: center;
    font-family: 'Open Sans', sans-serif;
    font-size: 20px;
  }
}
</style>
