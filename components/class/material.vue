<template>
  <div class="card rounded">
    <div class="card-body">
      <div class="row">
        <div class="col-1">
          <div
            class="bg-warning text-white text-center rounded-circle"
            id="icon"
          >
            <i class="far fa-clipboard"></i>
          </div>
        </div>
        <div class="col-10">
          <h6>{{ materialTitle }}</h6>
          <span>{{ date }}</span>
        </div>
        <div class="col-1">
          <div id="ellipsis" class="dropdown">
            <i
              class="fas fa-ellipsis-v"
              id="dropdownMenuLink"
              data-toggle="dropdown"
            ></i>
            <div class="dropdown-menu" aria-labelledby="dropdownMenuLink">
              <a class="dropdown-item" href="#">Copy Link</a>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    sender: {
      type: String,
      default: "Sender",
    },
    posting: {
      type: String,
      default: "Materi Dari Sender",
    },
    title: {
      type: String,
      default: "Title dari Sender",
    },
    date: {
      type: String,
      default: "",
    },
  },
  computed: {
    materialTitle() {
      return `${this.sender} memposting ${this.posting} terbaru: ${this.title}`;
    },
  },
};
</script>
<style scoped>
#icon {
  height: 50px;
  width: 50px;
}
#icon i {
  font-size: 1.7em;
  margin-top: 12px;
}
#ellipsis i {
  font-size: 1.5em;
  margin-top: 12px;
}
</style>