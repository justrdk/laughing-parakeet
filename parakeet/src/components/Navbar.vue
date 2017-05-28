<template>
<div class="ui fixed inverted menu navbar">
  <div class="ui container">
   <div class="left menu">
      <div class="header item borderless">
          Logo
      </div>
    </div>
    <a class="item borderless">
      Home
    </a>
     <a class="item borderless">
      Jobs
    </a>
     <a class="item borderless">
      About
    </a>
    <a class="item borderless">
      Departments
    </a>
    <a class="item borderless">
      Contact
    </a>
    <div class="right menu">
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
