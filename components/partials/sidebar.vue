<template>
  <div class="main-sidebar">
    <aside id="sidebar-wrapper">
      <div class="sidebar-brand">
        <a href="index.html">Stisla</a>
      </div>
      <div class="sidebar-brand sidebar-brand-sm">
        <a href="index.html">St</a>
      </div>
      <ul class="sidebar-menu">
        <li v-for="menu in menus" :key="menu">
          <nuxt-link :to="menu.link" class="nav-link"
            ><i :class="menu.icon"></i><span>{{ menu.name }}</span></nuxt-link
          >
        </li>
      </ul>
    </aside>
  </div>
</template>
<script>
export default {
  data() {
    return {
      menus: [
        { icon: "fas fa-home", name: "Kelas", link: "kelas" },
        { icon: "fas fa-calendar-alt", name: "Kalender", link: "kalender" },
        {
          icon: "fas fa-box",
          name: "Kelas yang diarsipkan",
          link: "arsip-kelas",
        },
        { icon: "fas fa-user-cog", name: "Setelan", link: "setelan" },
      ],
    };
  },
};
</script>