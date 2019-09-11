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
      <button>Login</button>
      <button>Signup</button>
    </div>
  </header>
</template>

<style lang="scss" scoped>
header {
  display: flex;
  align-items: center;
}

.logo {
  h2 {
    font-family: Russo One, sans-serif;

    span {
      color: var(--accent);
    }
  }
}
</style>

