<template>
  <div class="nav">
    <div class="nav__menu">
      <NuxtLink to="/" class="nav__menu--btn">Home</NuxtLink>
      <NuxtLink to="/about" class="nav__menu--btn">About us</NuxtLink>
    </div>

    <div class="nav__options">
       <NuxtLink to="/about" class="nav__menu--btn">Log In</NuxtLink>
    </div>
  </div>
</template>

<script>
export default {
  methods: {
  }
}
</script>

<style>
  .nav {
    height: 100%;
    min-height: 60px;
    max-height: 60px;

    background: rgb(45,59,61);

    -webkit-box-shadow: 0px 0px 10px 1px rgba(66, 68, 90, 1);
    -moz-box-shadow: 0px 0px 10px 1px rgba(66, 68, 90, 1);
    box-shadow: 0px 0px 10px 0px rgba(66, 68, 90, 1);

    display: flex;
    justify-content: space-between;
    align-items: center;

    padding: 0 10px 0 10px;
  }

  .nav__menu {
    height: 100%;
    min-width: 200px;
    display: flex;
    flex-wrap: wrap;
    align-items: center;
    justify-content: flex-start
  }

  .nav__options {
    height: 100%;
    min-width: 150px;
    display: flex;
    align-items: center;
    justify-content: flex-end;
  }

  .nav__menu--btn {
    padding: 0 10px 0 10px;
    height: 100%;
    min-width: 50px;
    display: flex;
    align-items: center;
    justify-content: center;
    color: whitesmoke;
    text-decoration: none;
  }

  .nav__menu--btn:hover {
    background-color: rgba(255, 255, 255, 0.3);
    transition: 0.33s;
  }
</style>
