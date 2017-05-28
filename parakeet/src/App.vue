<template>
  <div id="app">
    <Navbar></Navbar>
    <router-view></router-view>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar';

export default {
  name: 'app',
  components: {
    Navbar,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Yanone+Kaffeesatz:400,700');
@import url('https://fonts.googleapis.com/css?family=Open+Sans:400,700');
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
::-webkit-input-placeholder {
    color: #979797 !important;
    font-family: 'Open Sans', sans-serif;
    font-size: 12px;
    letter-spacing: 0.2px;
    text-align: left;
}
:-moz-placeholder {
   color: #979797 !important;
   font-family: 'Open Sans', sans-serif;
   font-size: 12px;
   letter-spacing: 0.2px;
   text-align: left;
   opacity:  1;
}
::-moz-placeholder {
  color: #979797 !important;
  font-family: 'Open Sans', sans-serif;
  font-size: 12px;
  letter-spacing: 0.2px;
  text-align: left;
   opacity:  1;
}
:-ms-input-placeholder {
   color: #979797 !important;
   font-family: 'Open Sans', sans-serif;
   font-size: 12px;
   letter-spacing: 0.2px;
   text-align: left;
}
::-ms-input-placeholder {
   color: #979797 !important;
   font-family: 'Open Sans', sans-serif;
   font-size: 12px;
   letter-spacing: 0.2px;
   text-align: left;

}
.no-padding {
  padding: 0px !important;
}
.white-text {
  color: #ffffff !important;
}
.align-left {
  text-align: left;
}
</style>
