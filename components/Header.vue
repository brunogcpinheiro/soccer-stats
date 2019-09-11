<template>
  <header>
    <div class="logo">
      <h2>
        Soccer
        <span>Stats</span>
      </h2>
    </div>
    <ul class="menu">
      <li>Stats</li>
      <li>Live</li>
      <li>Contacts</li>
    </ul>
    <div class="login">
      <button>Log in</button>
      <button>Sign up</button>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  display: flex;
  align-items: center;
  padding: 20px;
}

.logo {
  h2 {
    font-family: Russo One, sans-serif;
    margin: 0;
    padding: 0;

    span {
      font-family: Russo One, sans-serif;
      color: var(--accent);
    }
  }
}

.menu {
  display: flex;
  align-items: center;

  flex: 1;
}

.login {
  button {
    border: none;
    border-bottom: 2px solid #040607;
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
  }
}
</style>

