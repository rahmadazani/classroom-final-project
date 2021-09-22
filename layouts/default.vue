<template>
  <div id="app">
    <div class="main-wrapper">
      <PartialsNavbar />
      <PartialsSidebar />
      <div class="main-content">
        <section class="section">
          <div class="section-body" id="body"></div>
          <Nuxt />
        </section>
      </div>
      <PartialsFooter />
    </div>
  </div>
</template>
<style scoped>
#body {
  margin-bottom: 60px;
}
</style>
