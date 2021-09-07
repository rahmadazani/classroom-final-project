<template>
  <div>
    <h3>List Kelas Dalam Cart</h3>
    <ul>
      <li v-for="(cart, i) in listCart" :key="i">{{ cart }}</li>
    </ul>
    <hr />
    <elements-floating-button @click.native="addClass" />
    <div class="row">
      <div v-for="(item, i) in classes" :key="i" class="col-4">
        <card
          :title="item.title"
          :description="item.description"
          :img="item.img"
          @add-to-cart="updateCart"
        />
      </div>
    </div>
    <button class="btn btn-warning" type="button" @click="addClass">
      Tambah Kelas
    </button>
    <div class="card" style="height: 70vh">
      <div class="container mt-3">
        <input v-model="name" class="form-control" />
        <p>Ini adalah {{ name }}</p>
        <hr />
        <textarea v-model="desc" class="form-control"></textarea>
        <p style="white-space: pre-line">{{ desc }}</p>
        <hr />
        <select v-model="location" class="custom-select">
          <option value="" selected disabled>Open this select menu</option>
          <option
            v-for="province in provinces"
            :key="province"
            :value="province"
          >
            {{ province }}
          </option>
        </select>
        <p>{{ location }}</p>
        <hr />
        <h6>V-IF</h6>
        <h4 v-if="location == 'Jawa Barat'">Di Jawa Barat ada Gedung Sate</h4>
        <h4 v-else-if="location == 'Sumatera Utara'">
          Di Sumatera Utara ada Istana Maimun
        </h4>
        <h6>V-SHOW</h6>
        <h4 v-show="location == 'Jawa Barat'">Di Jawa Barat ada Gedung Sate</h4>
        <h4 v-show="location == 'Sumatera Utara'">
          Di Sumatera Utara ada Istana Maimun
        </h4>
      </div>
    </div>
  </div>
</template>
<script>
// import card from "~/components/card.vue";
export default {
  //  components: { card },
  data() {
    return {
      name: "",
      desc: "",
      location: "",
      provinces: ["Jawa Barat", "Sumatera Utara", "DKI Jakarta", "Papua"],
      classes: [
        {
          title: "Fullstack 4",
          description: "Description.......",
          img: "https://www.seekpng.com/png/detail/140-1407346_google-classroom-logo-google-classroom-icon.png",
        },
        {
          title: "Data Scientist 4",
          description: "Description.......",
          img: "https://rencanamu.id/assets/file_uploaded/editor/1500900879-data-scien.jpg",
        },
        {
          title: "Digital Marketing 4",
          description: "Description.......",
          img: "https://brankasbro.id/wp-content/uploads/2020/09/7.jpg",
        },
        {
          title: "Data Engineer 4",
          description: "Description.......",
        },
      ],
      listCart: [
        "Fullstack 4",
        "Data Scientist 4",
        "Digital Marketing 4",
        "Data Engineer 4",
      ],
    };
  },
  methods: {
    updateCart(title) {
      this.listCart.push(title); //ngepush biar bisa di cetak di web
    },
    //  methods: {
    addClass() {
      this.classes.push({
        title: "Kelas Tambahan",
        description: "deskripsi kelas tambahan",
      });
    },
  },
};
</script>