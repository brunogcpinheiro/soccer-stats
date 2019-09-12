<template>
  <div class="main">
    <div class="league">
      <img src="~assets/england.svg" alt="League">
      <small>Premiere League</small>
    </div>

    <div class="match">
      <div class="teams home">
        <img src="~assets/chelsea.svg" alt="Home team">
      </div>
      <span>vs</span>
      <div class="teams away">
        <img src="~assets/man-united.svg" alt="Away team">
      </div>
    </div>

    <div class="match-info"></div>
  </div>
</template>

<style lang="scss" scoped>
.main {
  background: var(--background-lighter);
  width: 300px;
  height: 350px;
  display: flex;
  flex-direction: column;
  padding: 10px;
}

.league {
  display: flex;
  align-items: center;

  img {
    width: 14px;
    height: 14px;
  }
  small {
    color: var(--foreground-contrast);
    margin-left: 5px;
  }
}

.match {
  display: flex;
  align-items: center;
  justify-content: space-around;
  margin-top: 20px;

  span {
    font-family: Russo one, sans-serif;
    font-weight: bold;
    font-style: italic;
  }

  .teams {
    background: var(--background-contrast);
    border-radius: 50%;
    width: 110px;
    height: 110px;
    padding: 10px;

    img {
      width: 100%;
    }
  }
}
</style>

