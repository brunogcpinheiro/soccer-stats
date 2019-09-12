<template>
  <div id="main">
    <h2>
      Live
      <span>Matches</span>
    </h2>

    <div class="cards-list">
      <CardMatch
        v-for="({ id, homeName, awayName, homeScore, awayScore, homeIcon, awayIcon, leagueIcon }) in matches"
        :key="id"
        :homeTeamName="homeName"
        :awayTeamName="awayName"
        :homeTeamScore="homeScore"
        :awayTeamScore="awayScore"
        :homeTeamIcon="homeIcon"
        :awayTeamIcon="awayIcon"
        :leagueIcon="leagueIcon"
      />
    </div>
  </div>
</template>

<script>
import CardMatch from "@/components/CardMatch.vue";
import PremierLeague from "@/assets/premier.svg";
import City from "@/assets/city.svg";
import United from "@/assets/man-united.svg";
import Arsenal from "@/assets/arsenal.svg";
import Leicester from "@/assets/leicester.svg";
import Liverpool from "@/assets/liverpool.svg";
import Chelsea from "@/assets/chelsea.svg";

export default {
  components: {
    CardMatch
  },
  data: () => ({
    matches: [
      {
        id: "1",
        homeName: "Manchester City",
        awayName: "Manchester United",
        homeScore: "3",
        awayScore: "1",
        homeIcon: City,
        awayIcon: United,
        leagueIcon: PremierLeague
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
</style>

