<template>
  <div>
    <section>
      <slot name="header"> </slot>
    </section>
    <section class="row">
      <div class="col-md-3">
        <slot name="coming"></slot>
      </div>
      <div class="col-md-9">
        <slot name="materials"></slot>
      </div>
    </section>
  </div>
</template>