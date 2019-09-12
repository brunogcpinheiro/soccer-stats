<template>
  <div class="box">
    <div class="info">
      <h1>Best player of the round!</h1>
      <p>27 gols and 4 assistances in this season!</p>
      <h4>Cristiano Ronaldo</h4>
      <h2>
        Overall:
        <span>95</span>
      </h2>
    </div>
    <div class="player">
      <img src="~assets/cristiano.png" alt="Best player">
    </div>
  </div>
</template>

<style lang="scss" scoped>
.box {
  background-color: var(--accent);
  width: 100%;
  margin: 25px;
  border-radius: 10px;
  display: flex;
  justify-content: space-between;

  .info {
    flex: 4;
    margin: 30px;
    display: flex;
    flex-direction: column;
    justify-content: space-around;

    h1 {
      text-transform: uppercase;
      font-family: Russo one, sans-serif;
    }

    p {
      flex: 3;
    }

    h4 {
      font-size: 3rem;
      color: var(--shined);
      flex: 2;
    }

    h2 {
      font-size: 2rem;

      span {
        color: var(--shined);
      }
    }
  }

  .player {
    width: 100%;
    height: 100%;
    flex: 1;

    img {
      width: 240px;
      float: right;
      margin-top: -30px;
    }
  }
}
</style>

