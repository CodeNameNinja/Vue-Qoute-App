<template>
  <div class="row">
    <div class="col sm 12">
      <h3>Qoutes Added</h3>

      <div class="progress">
        <div
          class="progress-bar"
          role="progressbar"
          aria-valuenow="60"
          aria-valuemin="0"
          aria-valuemax="100"
          :style="{width: (qouteCount / maxQoutes) * 100 + '%'}"
        >{{qouteCount}} / {{maxQoutes}}</div>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  props: ["qouteCount", "maxQoutes"],
};
</script>

<style>
</style>