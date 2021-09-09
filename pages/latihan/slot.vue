<template>
  <div>
    <h1>Latihan Slot</h1>
    <hr />
    <class-detail-layout>
      <template v-slot:header>
        <h1 class="bg-primary">Ini Header Untuk Detail Layout</h1>
      </template>
      <template v-slot:coming>
        <p class="bg-warning">Untuk Coming</p>
      </template>
      <template v-slot:materials>
        <h1 class="bg-info">List Materi</h1>
      </template>
    </class-detail-layout>
    <elements-button> <i class="fas fa-user-plus"></i> Daftar </elements-button>
  </div>
</template>