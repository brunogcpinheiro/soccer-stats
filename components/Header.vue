<template>
  <header>
    <div class="logo">
      <h2>
        Sports
        <span>Stats</span>
      </h2>
    </div>
    <ul class="menu">
      <li v-for="({ route, title, active }) in menu" :key="route" :class="{active}">{{ title }}</li>
    </ul>
    <div class="login">
      <button>Log in</button>
      <button>Sign up</button>
    </div>
  </header>
</template>

<script>
export default {
  data: () => ({
    menu: [
      {
        route: "/",
        title: "Games",
        active: true
      },
      {
        route: "/live",
        title: "Live",
        active: false
      },
      {
        route: "/contacts",
        title: "Contacts",
        active: false
      }
    ]
  })
};
</script>


<style lang="scss" scoped>
header {
  display: flex;
  align-items: center;
  padding: 0 20px;
}

.logo {
  h2 {
    font-family: Russo One, sans-serif;
    margin: 0;
    padding: 0;

    span {
      font-family: Russo One, sans-serif;
      color: var(--accent);
      font-weight: bold;
    }
  }
}

.menu {
  display: flex;
  align-items: center;
  flex: 1;

  > li {
    margin-left: 50px;
    cursor: pointer;
    color: var(--foreground-contrast);
  }

  .active {
    color: var(--foreground);
    font-weight: bold;
  }
}

.login {
  button {
    border: none;
    border-bottom: 2px solid var(--shined);
    background: var(--background-contrast);
    border-radius: 2px;
    padding: 7px 18px;
    color: var(--foreground);
    text-transform: uppercase;
    font-weight: bold;

    &:last-child {
      margin-left: 10px;
      background-color: var(--accent);
    }

    &:hover {
      animation: pulse 0.5s ease-in;
    }
  }
}
</style>

