<template>
  <div class="header-container">
    <!-- Left Section: Publication Info -->
    <div class="publication-info">
      <p>Supscription Information: 1866 237 937</p>

      <p>
        Weather: <span class="weather">{{ temperature }}</span
        >°F
      </p>
      <p>Current time: {{ timestamp }}</p>
    </div>

    <!-- Center Section: Newspaper Name -->
    <div class="newspaper-name">
      <p>Arkham Asylum Issue</p>
    </div>

    <!-- Right Section: Daily Quote -->
    <div class="container">
      <div class="daily-quote">
        <p>{{ title }}</p>
      </div>
    </div>
  </div>
</template>

<style scoped>
.header-container {
  display: flex;
  justify-content: space-between;
  height: 10vh; /* 10% of the viewport height */
}

.publication-info {
  width: 20%;
  font-family: "Old Newspaper Types", serif; /* Assuming you have this font available */
  font-size: 8px;
  /**/
  margin: 0;
  height: 5vh; /* 10% of the viewport height */

  top: 50%;
}

.newspaper-name {
  width: 60%;
  font-family: "Old Newspaper Types", serif;
  text-align: center;
  font-size: xx-large;
  /**/
  margin: 0;

  top: 100%;
}

.daily-quote {
  border: 1px solid black;
  text-align: center;
  font-family: "Old Newspaper Types", serif;
  font-size: xx-small;
  /**/
  margin: 0;
  margin-right: 25px;
  margin-top: 10px;
  top: 50%;
  padding-left: 10px;
  padding-right: 10px;
}
.newspaper-name,
.daily-quote .container {
  display: flex;
  align-items: center; /* Centers text vertically */
  justify-content: center; /* Centers text horizontally */
}
.container {
  width: 20%;
  display: flex;
  align-items: center; /* Centers text vertically */
  justify-content: center; /* Centers text horizontally */
}
</style>

<script setup>
import { ref, onMounted } from "vue";
//weather part
let temperature = ref(null);
let timestamp = ref(null);
//poetry part
let title = ref(null);
//
const url =
  "https://yahoo-weather5.p.rapidapi.com/weather?location=sunnyvale&format=json&u=f";
const options = {
  method: "GET",
  headers: {
    "X-RapidAPI-Key": "6a3dbc5b0dmsh65f22b45a5928dbp1a69f1jsn62d8d50826d3",
    "X-RapidAPI-Host": "yahoo-weather5.p.rapidapi.com",
  },
};

const url2 = "https://poetrydb.org/author/Edgar Allan Poe/title";
//
const url3 = "http://worldtimeapi.org/api/timezone/Asia/Taipei";
//
function getRandomInt(min, max) {
  min = Math.ceil(min); // Ensure the minimum is rounded up if necessary
  max = Math.floor(max); // Ensure the maximum is rounded down if necessary
  return Math.floor(Math.random() * (max - min + 1)) + min; // The maximum is inclusive and the minimum is inclusive
}

//
onMounted(async () => {
  const randomInt = getRandomInt(2, 50);
  try {
    //weather part
    const response = await fetch(url, options);
    const data = await response.json(); // assuming you want to parse the JSON response
    console.log(data); // log the parsed data
    temperature.value = data.current_observation.condition.temperature;

    //poet part
    const response2 = await fetch(url2);
    const data2 = await response2.json(); // assuming you want to parse the JSON response
    title.value = data2[randomInt].title;
    console.log(title.value); // log the parsed data
    //time part
    const response3 = await fetch(url3);
    const data3 = await response3.json();
    timestamp.value = data3.datetime;
  } catch (error) {
    console.error(error);
  }
});
//50
</script>
