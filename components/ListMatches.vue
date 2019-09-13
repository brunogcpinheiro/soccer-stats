<template>
  <div id="main">
    <h2>
      Live
      <span>Matches</span>
    </h2>

    <div class="cards-list">
      <CardMatch
        v-for="({ id, homeName, awayName, homeScore, awayScore, homeIcon, awayIcon, leagueIcon, leagueName, active }) in matches"
        :key="id"
        :homeTeamName="homeName"
        :awayTeamName="awayName"
        :homeTeamScore="homeScore"
        :awayTeamScore="awayScore"
        :homeTeamIcon="homeIcon"
        :awayTeamIcon="awayIcon"
        :leagueIcon="leagueIcon"
        :leagueName="leagueName"
        :class="{active}"
      />
    </div>
  </div>
</template>

<script>
import CardMatch from "@/components/CardMatch.vue";
import PremierLeague from "@/assets/premier.svg";
import LaLigaLeague from "@/assets/LaLiga.svg";
import City from "@/assets/city.svg";
import United from "@/assets/man-united.svg";
import Liverpool from "@/assets/liverpool.svg";
import Chelsea from "@/assets/chelsea.svg";
import Barcelona from "@/assets/barcelona.svg";
import RealMadrid from "@/assets/real-madrid.svg";

export default {
  components: {
    CardMatch
  },
  data: () => ({
    matches: [
      {
        id: Math.random(),
        homeName: "Manchester City",
        awayName: "Manchester United",
        homeScore: "3",
        awayScore: "1",
        homeIcon: City,
        awayIcon: United,
        leagueIcon: PremierLeague,
        leagueName: "Premier League",
        active: true
      },
      {
        id: Math.random(),
        homeName: "Liverpool",
        awayName: "Chelsea",
        homeScore: "2",
        awayScore: "0",
        homeIcon: Liverpool,
        awayIcon: Chelsea,
        leagueIcon: PremierLeague,
        leagueName: "Premier League",
        active: false
      },
      {
        id: Math.random(),
        homeName: "Barcelona",
        awayName: "Real Madrid",
        homeScore: "4",
        awayScore: "1",
        homeIcon: Barcelona,
        awayIcon: RealMadrid,
        leagueIcon: LaLigaLeague,
        leagueName: "La Liga",
        active: false
      }
    ]
  })
};
</script>


<style lang="scss" scoped>
#main {
  padding-top: 25px;

  h2 {
    color: var(--foreground);
    span {
      font-weight: 300;
      color: var(--foreground-contrast);
      opacity: 0.5;
    }
  }
}

.cards-list {
  display: flex;
  align-items: center;
  justify-content: space-around;
  flex-wrap: wrap;
  padding: 20px 0;
}

.active {
  border: 2px solid var(--accent);
}
</style>

