<template>
  <div v-for="(item, index) in proPdata" :key="index">
    <div class="wapper" :class="{ 'mb-5': !item.see_complition }">
      <div class="row mb-3">
        <div class="col-md-12">
          <div class="row">
            <div class="col-md-2 text-center pt-2">
              <img :src="item.flag_url" alt="flag" width="40" height="40" />
            </div>
            <div class="col-md-7 text-start">
              <h5 class="pt-3 ps-2">{{ item.league_name }}</h5>
            </div>
            <div class="col-md-2 text-end pt-2">
              <span class="green"><i class="far fa-star"></i></span>
            </div>
          </div>
        </div>
      </div>
      <div v-for="(match, index) in item.match_result" :key="index">
        <div class="row py-2 ps-4">
          <div class="col-md-2">
            <span class="fw-bolder gray">{{ match.status }}</span>
          </div>
          <div class="col-md-8">
            <h5 :class="{ 'fw-bolder': match.win == '1' }">
              {{ match.first_team }}
              <i
                v-if="match.red_flag == '1'"
                class="fas fa-square-full red"
              ></i>
            </h5>
            <h5 :class="{ 'fw-bolder': match.win == '2' }">
              {{ match.sec_team }}
              <i
                v-if="match.red_flag == '2'"
                class="fas fa-square-full red"
              ></i>
            </h5>
          </div>
          <div class="col-md-2">
            <h6>{{ match.first_team_score }}</h6>
            <h6>{{ match.sec_team_score }}</h6>
          </div>
        </div>
        <hr v-if="index != item.match_result.length - 1" />
      </div>
    </div>
    <div class="row" v-if="item.see_complition">
      <div class="col-md-4 offset-md-8 wapper-competition1">
        <h6>See the competition</h6>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  name: "Score",
  props: {
    proPdata: {
      type: Object,
      required: true,
    },
  },
  data() {
    return {};
  },
};
</script>

<style scoped>
.wapper {
  background: #fff;
  border-radius: 5px;
  border: 1px solid #e0dfdf;
}
.wapper-competition1 {
  background: #fff;
  padding: 10px 20px;
  width: 24%;
  color: #00b232;
  font-weight: bold;
  margin-bottom: 25px;
  border: 1px solid #e0dfdf;
}
.gray {
  color: gray;
}
.green {
  color: #00b232;
}
.red {
  color: red;
}
</style>