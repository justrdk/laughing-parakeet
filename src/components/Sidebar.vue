<template>
  <div class="ui sidebar inverted vertical menu">
      <div class="header item borderless">
        Logo
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
      <div class="item search-item borderless">
        <div class="ui input">
          <input type="text" placeholder="SEARCH FOR JOBS BY KEYWORD">
        </div>
      </div>
  </div>
</template>
<script>
export default {
  name: 'sidebar',
};
</script>
