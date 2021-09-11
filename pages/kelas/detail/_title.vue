<template>
  <div>
    <class-detail-layout>
      <template v-slot:header>
        <class-jumbotron />
      </template>
      <template v-slot:materials>
        <class-material
          v-for="(material, i) in listMaterial"
          :key="i"
          :sender="material.sender"
          :posting="material.posting"
          :title="material.title"
          :date="material.date"
        />
      </template>
      <template v-slot:coming>
        <class-coming />
      </template>
    </class-detail-layout>
  </div>
</template>
<script>
export default {
  data() {
    return {
      listMaterial: [
        {
          sender: "SPV class",
          posting: "materi",
          title: "Basic HTML",
          date: "08 September",
        },
        {
          sender: "SPV class",
          posting: "materi",
          title: "Basic CSS",
          date: "09 September",
        },
        {
          sender: "SPV class",
          posting: "materi",
          title: "Basic Javascript",
          date: "10 September",
        },
        {
          sender: "SPV class",
          posting: "materi",
          title: "Web Static",
          date: "11 September",
        },
        {
          sender: "SPV class",
          posting: "materi",
          title: "Data Binding",
          date: "12 September",
        },
        {
          sender: "SPV class",
          posting: "materi",
          title: "Backend Programming",
          date: "13 September",
        },
        {
          sender: "SPV class",
          posting: "materi",
          title: "Deployment",
          date: "14 September",
        },
      ],
    };
  },
};
</script>
