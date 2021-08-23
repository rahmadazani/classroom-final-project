<template>
  <div>
    <h3>LIST CLASS</h3>
    <div class="row">
      <div v-for="i in 3" :key="i" class="col-3 ">
        <card />
      </div>
      </div>
    </div>
  </div>
</template>