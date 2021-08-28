<template>
  <div>
    <h4>Watcher yes/no question</h4>
    <input type="text" class="form-control" v-model="question" />
    <p>{{ answer }}</p>
    <img :src="img" alt="" srcset="" />
  </div>
</template>
<script>
export default {
  data() {
    return {
      question: "",
      answer: "",
      img: "",
    };
  },
  methods: {
    getAnswer() {
      this.answer = "Thinking....";
      this.img = "";
      this.$axios
        .get("https://yesno.wtf/api")
        .then((response) => {
          this.answer = response.data.answer;
          this.img = response.data.image;
        })
        .catch((err) => {
          this.answer = "sorry...." + err;
        });
    },
  },
  watch: {
    question(newQuetion, oldQuetion) {
      if (newQuetion.indexOf("?") > -1) {
        this.getAnswer();
      }
    },
  },
};
</script>