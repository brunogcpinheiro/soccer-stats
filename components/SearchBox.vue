<template>
  <div class="search-box">
    <span>
      <img width="20" height="20" src="~assets/search-line.svg" alt="Search">
    </span>
    <input type="text" placeholder="Search">
  </div>
</template>

<style lang="scss" scoped>
.search-box {
  display: flex;
  align-items: center;
  background-color: var(--background-contrast);
  width: 100%;
  height: 50px;
  padding: 5px;
  border-radius: 5px;

  span {
    margin: 0 5px;
  }

  input {
    background: transparent;
    border: none;
    margin-left: 3px;
    color: var(--foreground);
    flex: 1;

    &::placeholder {
      color: var(--foreground-contrast);
    }
  }
}
</style>
