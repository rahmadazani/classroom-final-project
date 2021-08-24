<template>
  <div>
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
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      name: "",
      desc: "",
      location: "",
      provinces: ["Jawa Barat", "Sumatera Utara", "DKI Jakarta", "Papua"],
    };
  },
};
</script>