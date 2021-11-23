<template>
  <div class="map">
    <div id="map"></div>
  </div>
</template>
<style>
body {
  margin: 0;
  padding: 0;
}
#map {
  position: absolute;
  top: 0;
  bottom: 0;
  height: 600px;
  width: 100%;
}
</style>

<script>
/* global mapboxgl */

export default {
  mounted: function () {
    this.createMap();
  },
  methods: {
    createMap: function () {
      mapboxgl.accessToken = process.env.VUE_APP_API;
      var map = new mapboxgl.Map({
        container: "map", // container ID
        style: "mapbox://styles/mapbox/streets-v11", // style URL
        center: [-81, 34], // starting position [lng, lat]
        zoom: 9, // starting zoom
      });
      console.log(map);
    },
  },
};
</script>
