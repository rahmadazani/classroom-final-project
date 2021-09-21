<template>
  <div id="app">
    <div class="main-wrapper">
      <partials-navbar-detail />
      <div
        class="main-content"
        style="padding-left: 120px; padding-right: 120px"
      >
        <section class="section">
          <div class="section-body"></div>
          <Nuxt />
        </section>
      </div>
      <PartialsFooter />
    </div>
  </div>
</template>