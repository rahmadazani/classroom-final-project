<template>
  <div>
    <class-detail-layout>
      <template v-slot:header>
        <div class="text-center bg-primary text-white">
          <h3>Nama Kelas</h3>
        </div>
      </template>
      <template v-slot:materials>
        <div class="bg-danger h-100">
          <ul>
            <li>MATERI 1</li>
            <li>MATERI 2</li>
            <li>MATERI 3</li>
            <li>MATERI 4</li>
          </ul>
        </div>
      </template>
      <template v-slot:coming>
        <class-coming />
      </template>
    </class-detail-layout>
  </div>
</template>