<template>
  <div id="app">
    <Sidebar></Sidebar>
    <div class="pusher">
      <Navbar></Navbar>
      <router-view></router-view>
    </div>
  </div>
</template>

<script>
import Navbar from '@/components/Navbar';
import Sidebar from '@/components/Sidebar';

export default {
  name: 'app',
  components: {
    Navbar,
    Sidebar,
  },
};
</script>

<style>
@import url('https://fonts.googleapis.com/css?family=Yanone+Kaffeesatz:400,700');
@import url('https://fonts.googleapis.com/css?family=Open+Sans:400,700');
@media (max-width: 991px) {
  .desktop.only {
    display: none !important;
  }
  .mobile.only {
    display:block !important;
  }
}
@media (min-width: 992px) {
  .desktop.only {
    display: block !important;
  }
  .mobile.only {
    display:none !important;
  }
}
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
