<template>
  <div id="container">
    <div class="game-detail">
      <div class="field">
        <img src="~assets/etihad.jpg" alt="Etihad Stadium">
        <p>
          Etihad Stadium
          <small>(Manchester City)</small>
        </p>
        <p>Supporters: 48,325</p>
      </div>
      <hr>
      <div class="match">
        <img src="~assets/city.svg" alt="Man City">
        <span>3</span>
        <img src="~assets/man-united.svg" alt="Man City">
        <span>1</span>
      </div>
      <div class="match-info">
        <p>Gols</p>
        <div class="teams home-team">
          <p>Manchester City</p>
          <div class="players">
            <p>
              <img src="~assets/football.svg" alt="Gol">
              <img src="~assets/football.svg" alt="Gol"> Aguero
            </p>
            <p>
              <img src="~assets/football.svg" alt="Gol"> G. Jesus
            </p>
          </div>
        </div>
        <div class="teams away-team">
          <p>Manchester United</p>
          <div class="players">
            <p>
              <img src="~assets/football.svg" alt="Gol"> Lukaku
            </p>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
#container {
  width: 100%;
  height: 100%;
  padding: 25px 10px;
}

.game-detail {
  background: var(--background-lighter);
  width: 100%;
  height: 70%;
  color: var(--foreground-contrast);
  display: flex;
  flex-direction: column;
  align-items: center;
}

.field {
  width: 100%;
  padding: 5px;
  display: flex;
  flex-direction: column;
  align-items: center;

  img {
    width: 100%;
    border: 3px solid var(--background-contrast);
  }

  p {
    padding: 5px;
    font-size: 0.875rem;
  }
}

hr {
  height: 2px;
  border: 1px solid var(--accent);
  width: 80%;
}

.match {
  display: flex;
  align-items: center;
  margin: 20px 0;
  img {
    width: 48px;
    height: 48px;
  }

  span {
    margin: 0 10px;
    font-size: 1.7rem;
  }
}

.match-info {
  display: flex;
  flex-direction: column;
  align-items: center;
  margin-top: 30px;

  .teams {
    display: flex;
    flex-direction: column;
    align-items: center;
    padding-top: 20px;

    .players {
      color: var(--foreground-darker);
      font-size: 0.7rem;

      p {
        padding-top: 10px;
      }

      img {
        width: 10px;
        height: 10px;
      }
    }
  }
}
</style>

