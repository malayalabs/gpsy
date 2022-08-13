<script>
import {
  LMap,
  LTileLayer,
} from '@vue-leaflet/vue-leaflet';
import 'leaflet/dist/leaflet.css';

export default {
  components: {
    LMap,
    LTileLayer,
  },
  data() {
    return {
      zoom: 5,
    };
  }
}
</script>

<template>
  <div id="map-container">
    <l-map
      v-model="zoom"
      v-model:zoom="zoom"
      :center="[14.311442, 120.965403]"
    >
      <l-tile-layer
        url="https://{s}.tile.openstreetmap.org/{z}/{x}/{y}.png"
      ></l-tile-layer>
    </l-map>
  </div>
</template>

<style scoped>
  #map-container {
    width: 100vw;
    height: 100vh;
  }
</style>
