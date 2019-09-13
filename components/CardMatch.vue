<template>
  <div class="hvr-reveal main">
    <div class="league">
      <img :src="leagueIcon" alt="League">
      <small>{{leagueName}}</small>
      <div class="badge">
        <p>LIVE</p>
      </div>
    </div>

    <div class="match">
      <div class="teams home">
        <img :src="homeTeamIcon" alt="Home team">
      </div>
      <span>vs</span>
      <div class="teams away">
        <img :src="awayTeamIcon" alt="Away team">
      </div>
    </div>

    <div class="time">
      <small>2nd Half 72'</small>
      <div class="halfs">
        <div class="first-half"></div>
        <div class="second-half"></div>
      </div>
    </div>

    <div class="match-info">
      <div class="home-info">
        <p>{{ homeTeamName }}</p>
        <span>{{ homeTeamScore }}</span>
      </div>
      <div class="away-info">
        <p>{{ awayTeamName }}</p>
        <span>{{ awayTeamScore }}</span>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: {
    leagueIcon: {
      type: String,
      required: true
    },
    leagueName: {
      type: String,
      required: true
    },
    homeTeamIcon: {
      type: String,
      required: true
    },
    awayTeamIcon: {
      type: String,
      required: true
    },
    homeTeamName: {
      type: String,
      required: true
    },
    awayTeamName: {
      type: String,
      required: true
    },
    homeTeamScore: {
      type: String,
      required: true
    },
    awayTeamScore: {
      type: String,
      required: true
    }
  }
};
</script>


<style lang="scss" scoped>
.hvr-reveal {
  display: inline-block;
  vertical-align: middle;
  -webkit-transform: perspective(1px) translateZ(0);
  transform: perspective(1px) translateZ(0);
  box-shadow: 0 0 1px rgba(0, 0, 0, 0);
  position: relative;
  overflow: hidden;
}
.hvr-reveal:before {
  content: "";
  position: absolute;
  z-index: -1;
  left: 0;
  right: 0;
  top: 0;
  bottom: 0;
  border-color: var(--accent);
  border-style: solid;
  border-width: 0px;
  -webkit-transition-property: border-width;
  transition-property: border-width;
  -webkit-transition-duration: 0.1s;
  transition-duration: 0.1s;
  -webkit-transition-timing-function: ease-out;
  transition-timing-function: ease-out;
}
.hvr-reveal:hover:before,
.hvr-reveal:focus:before,
.hvr-reveal:active:before {
  -webkit-transform: translateY(0);
  transform: translateY(0);
  border-width: 5px;
}

.main {
  background: var(--background-lighter);
  width: calc((100% / 3) - 10px);
  height: 100%;
  display: flex;
  flex-direction: column;
  padding: 10px;
  cursor: pointer;

  &:hover {
    background: var(--background-hover);
    transition: all 0.4s ease;
  }
}

.league {
  display: flex;
  align-items: center;

  img {
    width: 36px;
    height: 36px;
  }
  small {
    color: var(--foreground-contrast);
    margin-left: 5px;
    flex: 1;
  }
  .badge {
    background: var(--dark-red);
    padding: 3px 6px;
    font-size: 0.7rem;
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
    width: 80px;
    height: 80px;
    padding: 7px;

    img {
      width: 100%;
      height: 100%;
    }
  }
}

.time {
  padding: 10px;

  .halfs {
    width: 100%;
    height: 10px;
    margin-top: 5px;
    display: flex;
    align-items: center;
    padding: 2px;
    border: 1px solid var(--background-contrast);

    .first-half {
      border: 2px solid var(--dark-red);
      width: 80%;
    }

    .second-half {
      border: 2px solid var(--light-red);
      width: 20%;
    }
  }
}

.match-info {
  border: 1px solid var(--background-contrast);
  border-radius: 5px;
  padding: 20px;
  margin-top: 20px;
  width: 100%;
  height: 100%;

  .home-info,
  .away-info {
    display: flex;
    align-items: center;
    justify-content: space-between;

    span {
      color: var(--shined);
    }
  }
}
</style>

