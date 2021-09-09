<template>
  <div>
    <h3>List Kelas Dalam Cart</h3>
    <ul>
      <li v-for="(cart, i) in listCart" :key="i">{{ cart }}</li>
    </ul>
    <hr />
    <elements-floating-button @join-class="joinClass" />
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
  </div>
</template>
<script>
export default {
  data() {
    return {
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
    addClass() {
      this.classes.push({
        title: "Kelas Tambahan",
        description: "deskripsi kelas tambahan",
      });
    },
    joinClass(classCode) {
      alert("Selamat Kamu Bergabung Di" + classCode);
    },
  },
};
</script>