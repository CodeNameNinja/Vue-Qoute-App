<template>
  <div class="col-sm-6 col-md-4 col-lg-3">
      <div class="card panel-default">
          <div class="card-body qoute">
              <slot></slot>
          </div>
      </div>
  </div>
</template>

<script>

export default {

}
</script>

<style >
    .card-body{
        font-family: cursive;
        font-size: 24px;
        color: #6e6e6e;
    }
    .qoute{
        cursor: pointer;
    }
    .qoute:hover{
        background-color: #ffe2e2;
    }
</style>