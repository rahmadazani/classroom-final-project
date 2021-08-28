<template>
  <div class="container">
    <div>
      <label for="Password"></label>
      <input class="form-control" v-model="password" />
      <p>{{ checkPassword }}</p>
    </div>
    <hr />
    <div>
      <input class="form-control" v-model="firstName" placeholder="Firstname" />
      <input class="form-control" v-model="lastName" placeholder="Lastname" />
      <p>fullname : {{ fullname }}</p>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      password: "",
      firstName: "Rahmad",
      lastName: "Azani",
    };
  },
  computed: {
    checkPassword() {
      return this.password.length > 8
        ? this.password
        : "Password tidak boleh kurang dari 8 karakter";
    },
    fullname: {
      get() {
        return this.firstName + " " + this.lastName;
      },
      set(value) {
        const arrName = value.split(" ");
        this.firstName = arrName[0];
        this.lastName = arrName[arrName.length - 1];
      },
    },
  },
};
</script>