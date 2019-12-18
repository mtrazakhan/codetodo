<template>
  <header class="customHeader">
    <div class="headingDiv">
    <h1>My Todo</h1>
    </div>
    <div id="nav" class="linkDiv">
      <router-link to="/">Home</router-link> |
      <router-link to="/about">About</router-link>
    </div>
  </header>
</template>

<script>
export default {
  name: "Header"
}
</script>

<style scoped>
  .customHeader {
    background: #17a2b8;
  }
  .headingDiv {
    color: #fff;
    text-align: left;
    padding: 10px;
  }

  .customHeader a {
    color: #fff;
    padding-right: 5px;
    text-decoration: none;
  }

  .linkDiv{
    position: absolute;
    right: 30px;
    margin-top: -40px;
  }
</style>
