<template>
  <div class="container mt-5 mx-auto w-90" id="content">
    <div class="row mx-auto">
      <div class="col bg-light rounded p-5">
        <h1 class="my-2">
          <small>Weather <strong>Forecast</strong></small>
        </h1>
        <h3 class="my-2 font-italic"><small>Check weather below</small></h3>
        <div class="row mt-5 mx-auto">
          <table class="table">
            <thead class="contrast-text">
              <tr class="d-flex">
                <th class="col-2">Place</th>
                <th class="col-2">Weather</th>
                <th class="col-3">Temperature</th>
                <th class="col-3">Humidity</th>
                <th class="col-2">Details</th>
              </tr>
            </thead>
            <tbody>
              <tr class="d-flex" v-for="f in forecast" :key="f">
                <td class="col-2">{{ f.name }}</td>
                <td class="col-2">{{ f.weather[0].description }}</td>
                <td class="col-3">{{ f.main.temp }}°C</td>
                <td class="col-3">{{ f.main.humidity }}%</td>
                <td class="col-2">
                  <a href="#" class="btn btn-primary contrast-text border-0"
                    >Check</a
                  >
                </td>
              </tr>
            </tbody>
          </table>

          <div class="card bg-transparent border-0 mt-5">
            <div class="row">
              <input
                type="text"
                placeholder="City's name"
                v-model="new_city"
                class="ml-3"
              />
              <a
                @click="getWeather"
                class="
                  btn btn-primary
                  contrast-text
                  text-white
                  border-0
                  ml-3
                  font-weight-bold
                "
                >Add new place</a
              >
            </div>
            <small>{{ input_messsage }}</small>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>

<script>
//import cities from '../assets/city_list.json';

export default {
  name: "Home",
  components: {},
  data() {
    return {
      //city_list: cities,
      input_messsage: "",
      weather: {},
      api_key: "33b5ba68e4c4ecabdb4713be5f706a37",
      url_base: "https://api.openweathermap.org/data/2.5/weather?q=",
      new_city: "",
      forecast: [],
    };
  },
  methods: {
    getWeather() {
      fetch(
        `${this.url_base}${this.new_city}&units=metric&APPID=${this.api_key}`
      )
        .then((res) => {
          return res.json();
        })
        .then(this.addNewForecast)
        .catch((this.input_messsage = "Wrong input"));
    },
    addNewForecast(fetched) {
      this.weather = fetched;
      this.forecast.push(this.weather);
      this.new_city = "";
      this.input_messsage = "";
    },
  },
};
</script>

<style scoped>
#content {
  color: rgb(61, 50, 88);
}

.contrast-text {
  color: white;
  background-color: rgb(61, 50, 88);
}
</style>
