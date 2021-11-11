  <template>
  <ul class="nav nav-tabs mt-3" role="tablist">
    <li class="nav-item">
      <a class="nav-link active text-center" data-bs-toggle="tab" href="#all"
        >All</a
      >
    </li>
    <li class="nav-item">
      <a class="nav-link text-center" data-bs-toggle="tab" href="#live">Live</a>
    </li>
    <li class="nav-item">
      <a class="nav-link text-center" data-bs-toggle="tab" href="#favorites"
        >Favorites</a
      >
    </li>
  </ul>

  <!-- Tab panes -->
  <div class="tab-content gray">
    <div id="all" class="container tab-pane active">
      <br />
      <score :proPdata="match_data" />
    </div>
    <div id="live" class="container tab-pane fade">
      <br />
      <h3>Live</h3>
      <p>There will be UI of live tab</p>
    </div>
    <div id="favorites" class="container tab-pane fade">
      <br />
      <h3>Favorites</h3>
      <p>There will be UI of favorites tab</p>
    </div>
  </div>
</template>
<script>
import Score from "./Score.vue";
export default {
  components: { Score },
  name: "Tabs",
  data() {
    return {
      match_data: [],
    };
  },
  mounted() {
    this.match_data = [
      {
        flag_url:
          "https://icons.iconarchive.com/icons/wikipedia/flags/1024/FR-France-Flag-icon.png",
        league_name: "France- Copa de Le Liga",
        see_complition: true,
        match_result: [
          {
            first_team: "Monaco",
            sec_team: "Rennes",
            first_team_score: 1,
            sec_team_score: 1,
            status: "END",
            win: "1",
            tie: false,
            red_flag:'0'
          },
          {
            first_team: "Bordeaux",
            sec_team: "Le Havre AC",
            first_team_score: 1,
            sec_team_score: 0,
            status: "END",
            win: "1",
            tie: false,
            red_flag:'0'
          },
          {
            first_team: "PSG",
            sec_team: "EA Guingamp",
            first_team_score: 1,
            sec_team_score: 2,
            status: "END",
            win: "2",
            tie: false,
            red_flag:'0'
          },
        ],
      },
      {
        flag_url:
          "https://www.countryflags.com/wp-content/uploads/south-africa-flag-png-xl.png",
        league_name: "Afrique du sud- Premier League",
        see_complition: false,
        match_result: [
          {
            first_team: "Bidvest Wits",
            sec_team: "Kaizer Chiefs",
            first_team_score: 0,
            sec_team_score: 2,
            status: "END",
            win: "2",
            tie: false,
            red_flag:'1'
          },
          {
            first_team: "Maritzburg United",
            sec_team: "Free State Stars",
            first_team_score: 1,
            sec_team_score: 2,
            status: "END",
            win: "2",
            tie: false,
            red_flag:'0'
          },
        ],
      }
    ];
  },
};
</script>

<style scoped>
.gray {
  background: #f1f1f1;
  padding-bottom: 25px;
}

.nav-tabs .nav-link {
  color: black;
  border: none;
}
.nav-item {
  width: 33%;
}
.nav-tabs .nav-item.show .nav-link,
.nav-tabs .nav-link.active {
  border-bottom: 4px solid #00b232;
}
</style>