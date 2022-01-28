<template>
  <header>
    <div class="container-brand">
      <NuxtLink to="/">
        <img src="~/assets/images/logo.png" alt="logo" height="70" />
        <h1>Primakara <span>Developer</span></h1>
      </NuxtLink>
    </div>
    <nav class="desktop-nav">
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/about">About</NuxtLink>
      <NuxtLink to="/our-team">Our Team</NuxtLink>
    </nav>
  </header>
</template>

<style scoped lang="scss">
@import url("~/assets/styles/main.css");
header {
  align-items: center;
  display: flex;
  justify-content: space-between;
  padding: 8px 100px; // ! all parent elements must have padding like this

  .container-brand a {
    align-items: center;
    display: flex;
    gap: 2;
    text-decoration: none;

    h1 {
      color: rgb(80, 78, 78); // ! this is just a temporary color
      font-size: 25px;
      font-weight: 100;

      span {
        font-weight: 700;
      }
    }
  }

  .desktop-nav a {
    color: gray; // ! this is just a temporary color
    margin-left: 40px;
    text-decoration: none;
  }
}
</style>
