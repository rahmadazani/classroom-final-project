<template>
  <div>
    <div class="navbar-bg"></div>
    <nav class="navbar navbar-expand-lg main-navbar">
      <div id="classroom-text" class="btn">
        <h4>Google Classroom</h4>
      </div>
      <form class="form-inline mr-auto">
        <ul class="navbar-nav mr-3"></ul>
      </form>
      <elements-floating-button @join-class="joinClass" />
      <ul class="navbar-nav navbar-right">
        <li class="dropdown">
          <a
            href="#"
            data-toggle="dropdown"
            class="nav-link dropdown-toggle nav-link-lg nav-link-user"
          >
            <img
              alt="image"
              src="/assets/img/avatar/avatar-1.png"
              class="rounded-circle mr-1"
            />
            <div class="d-sm-none d-lg-inline-block">Masuk</div></a
          >
          <div class="dropdown-menu dropdown-menu-right">
            <a
              href="features-profile.html"
              class="dropdown-item has-icon text-success"
            >
              <i class="far fa-user"></i> Daftar
            </a>
            <a
              href="features-profile.html"
              class="dropdown-item has-icon text-primary"
            >
              <i class="far fa-user"></i> Login
            </a>
            <!-- <div class="dropdown-divider"></div>
             <a href="#" class="dropdown-item has-icon text-danger">
              <i class="fas fa-sign-out-alt"></i> Logout
            </a> -->
          </div>
        </li>
      </ul>
    </nav>
  </div>
</template>
<style scoped>
#classroom-text {
  color: rgb(10, 9, 9);
  margin-top: 40px;
  background-color: aliceblue;
}
</style>