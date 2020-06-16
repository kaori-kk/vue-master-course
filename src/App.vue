<template>
  <div id="app">
    <main>
      <div class="search-box">
        <input type="text" class="search-bar" placeholder="Search..."/>
        <div class="weather-wra">
          <div class="location-box">
            <div class="location">Northamption, UK</div>
            <div class="date">Monday 20 January 2020</div>
          </div>

          <div class="weather-box">
            <div class="temp">9℃</div>
            <div class="weather">Rain</div>
          </div>
        </div>
      </div>
    </main>
  </div>
</template>

<script>
export default {
  name: 'app',
  data () {
    return {
      api_key: '9987ae6ad93f5cd6acbf3b2ff18ac27d'
    }
  },
  methods: {
  }
}
</script>

<style>
  *{
    margin: 0;
    padding: 0;
    box-sizing:border-box;
  }

  body {
    font-family: "montserrat", sans-serif;
  }

  #app {
    background-image: url("./assets/cold-bg.png");
    background-size: cover;
    background-position: bottom;
    transition: 0.4s;

  }

  main {
    min-height: 100vh;
    padding: 25px;
    background-image: linear-gradient(to button, rgba(0,0,0,0.25), rgba(0,0,0,0.75))
  }

  .search-box{
    width: 100%;
    margin-bottom: 30px; 
  }

  .search-box .search-bar{
    display: block;
    width: 100%;
    padding: 15px;

    color: #313131;
    font-size: 20px;

    appearance: none;
    border: none;
    outline: none;
    background: none;

    box-shadow: 0px 0px 8px rgba(0,0,0,0.25);
    background-color: rgba(255, 255, 255, 0.5);
    border-radius: 0px 16px 0px 16px;
    transition: 0.5s;
  }

  .search-box .search-bar:focus{
    background-color: rgba(255,255,255,0.75);
    box-shadow: 0px 0px 16px rgba(0,0,0,0.25);
    border-radius: 16px 0px 16px 0px;
  }

  .location-box .location{
    margin-top: 20px;
    color: #222;
    font-weight: 500;
    font-size: 32px;
    text-align: center;
  }

  .location-box .date {
    color: #222;
    font-weight: 500;
    font-size: 20px;
    text-align: center;
    font-style: italic;
  }

  .weather-box{
    text-align: center;
  }

  .weather-box .temp {
    display: inline-block;
    padding: 10px 25px;
  }
</style>