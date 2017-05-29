<template>
  <div>
    <top-segment></top-segment>
    <form-segment></form-segment>
    <bottom-segment></bottom-segment>
    <footer-segment></footer-segment>
  </div>
</template>
<script>
import TopSegment from './TopSegment';
import FormSegment from './FormSegment';
import BottomSegment from './BottomSegment';
import FooterSegment from './FooterSegment';

export default {
  name: 'main',
  components: {
    TopSegment,
    FormSegment,
    BottomSegment,
    FooterSegment,
  },
};
</script>
