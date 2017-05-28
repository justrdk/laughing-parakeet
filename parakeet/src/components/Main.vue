<template>
  <div>
    <top-segment></top-segment>
    <form-segment></form-segment>
    <bottom-segment></bottom-segment>
  </div>
</template>
<script>
import TopSegment from './TopSegment';
import FormSegment from './FormSegment';
import BottomSegment from './BottomSegment';

export default {
  name: 'main',
  components: {
    TopSegment,
    FormSegment,
    BottomSegment,
  },
};
</script>
