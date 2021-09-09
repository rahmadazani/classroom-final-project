<template>
  <div>
    <div class="row">
      <div v-for="(item, i) in listClass" :key="i" class="col-md-3">
        <card :title="item.title" :description="item.description" />
      </div>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      listClass: [
        { title: "Fullstack 4", description: "Fullstack 4 description...." },
        {
          title: "Data Scientist 4",
          description: "Data Scientist 4 descriptionnyaa....",
        },
        {
          title: "Digital Marketing 4",
          description: "Data Engineer 4 description....",
        },
      ],
    };
  },
};
</script>