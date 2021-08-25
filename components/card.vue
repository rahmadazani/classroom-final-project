<template>
  <div class="card">
    <img :src="img" class="card-img-top" alt="gambar kelas" />
    <div class="card-body">
      <h4>{{ title }}</h4>
      <p class="card-text">{{ description }}</p>
    </div>
    <div class="card-footer">
      <button type="button" class="btn btn-primary w-100 text-center">
        ADD TO CART
      </button>
    </div>
  </div>
</template>
<script>
export default {
  props: {
    description: {
      type: String,
      default: "Description",
    },
    title: {
      type: String,
      default: "Title",
    },
    img: {
      type: String,
      default:
        "https://images.glints.com/unsafe/glints-dashboard.s3.amazonaws.com/company-logo/dd7ca8d847af8f7796144a57ba9e1106.png",
    },
  },
};
</script>