<template>
  <div>
    <top-segment></top-segment>
    <form-segment></form-segment>
  </div>
</template>
<script>
import TopSegment from './TopSegment';
import FormSegment from './FormSegment';

export default {
  name: 'main',
  components: {
    TopSegment,
    FormSegment,
  },
};
</script>
