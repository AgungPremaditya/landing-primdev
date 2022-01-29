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
    <nav class="mobile-nav hide">
      <NuxtLink to="/">Home</NuxtLink>
      <NuxtLink to="/about">About</NuxtLink>
      <NuxtLink to="/our-team">Our Team</NuxtLink>
    </nav>
  </header>
</template>

<style scoped lang="scss">
@import url("../assets/styles/main.css");
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
      color: var(--primary-gray);
      font-size: 25px;
      font-weight: 100;

      span {
        font-weight: 700;
      }
    }
  }

  .desktop-nav a {
    color: var(--secondary-gray);
    font-size: 14px;
    margin-left: 40px;
    text-decoration: none;
    transition: ease 1s all;
  }

  .desktop-nav a:hover {
    color: var(--primary-gray);
  }

  nav.hide {
    display: none;
  }
}

@media only screen and (max-width: 768px) {
  header {
    padding: 8px 50px;

    .container-brand a h1 {
      font-size: 18px;
    }

    .desktop-nav a {
      margin-left: 20px;
    }
  }
}

@media only screen and (max-width: 768px) {
  header {
    .desktop-nav {
      display: none;
    }
  }
}
</style>
