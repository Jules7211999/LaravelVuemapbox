<template>
  <div id="mapContainer"></div>
</template>

<script>
import mapboxgl from "mapbox-gl";

export default {
  name: "BaseMap",
  data() {
    return {
      accessToken: "pk.eyJ1IjoianVsZXNsZW9tZWwiLCJhIjoiY2ttYnJhZTU4MDNucjJ2bGozd3lhMjI2ciJ9.pJW1MGbeoeYe-jbXaA1XgQ",
    };
  },
  mounted() {
    mapboxgl.accessToken = this.accessToken;

    new mapboxgl.Map({
      container: "mapContainer",
      style: "mapbox://styles/mapbox/streets-v11",
      center: [103.811279, 1.345399],
      zoom: 12,
      maxBounds: [
        [103.6, 1.1704753],
        [104.1, 1.4754753],
      ],
    });
  },
};
</script>

<style>
#mapContainer{
 width: 100vh;
 height: 1000px;
 background-color: black;
}
</style>

