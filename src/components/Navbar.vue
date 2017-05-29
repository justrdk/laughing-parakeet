<template>
<div class="ui fixed inverted main menu navbar">
  <div class="ui container">
   <div class="left menu">
      <div class="desktop only header item borderless">
          Logo
      </div>
      <div class="mobile only header item borderless hidden" @click="toggleSidebar">
          <i class="icon content"></i>
      </div>
    </div>
    <a class="desktop only item borderless">
      Home
    </a>
     <a class="desktop only item borderless">
      Jobs
    </a>
     <a class="desktop only item borderless">
      About
    </a>
    <a class="desktop only item borderless">
      Departments
    </a>
    <a class="desktop only item borderless">
      Contact
    </a>
    <div class="desktop only right menu">
      <div class="item search-item borderless">
        <div class="ui input">
          <input type="text" placeholder="SEARCH FOR JOBS BY KEYWORD">
        </div>
      </div>
    </div>
  </div>
</div>
</template>

<script>
  export default {
    name: 'navbar',
    methods: {
      toggleSidebar() {
        $('.ui.sidebar').sidebar('toggle');
      },
    },
  };
</script>

<style lang="scss" scoped>
.navbar {
  .container {
    padding: 5px;
  }
  .item.borderless {
    border: none !important;
  }
  .right.menu {
    .search-item {
      width: 310px;
      height: 39px;
      font-size: 12px;
      .ui.input {
        font-weight: 600;
        text-align: left;
        color: rgba(0, 0, 0, 0.5);
        letter-spacing: 0.2px;
      }
    }
  }
}
</style>
