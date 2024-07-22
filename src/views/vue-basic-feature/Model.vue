<template>
  <ion-page>
    <ion-header>
      <ion-toolbar color="primary">
        <ion-buttons slot="start">
          <ion-button @click="back">
            <ion-icon slot="icon-only" :icon="arrowBackOutLine"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title>Modal</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Modal</ion-title>
        </ion-toolbar>
      </ion-header>

      <div class="padding">
        <p>{{ name }}</p>
        <p>{{ address }}</p>

        <ion-input
          label="Nama"
          v-model="name"
          label-placement="floating"
          fill="solid"
          placeholder="Masukan Nama"
        ></ion-input>

        <br />

        <ion-input
          label="Nama"
          v-model="name"
          label-placement="floating"
          fill="solid"
          placeholder="Masukan Nama"
        ></ion-input>

        <br />

        <ion-input
          label="Nama"
          v-model="name"
          label-placement="floating"
          fill="solid"
          placeholder="Masukan Nama"
        ></ion-input>
      </div>
    </ion-content>
  </ion-page>
</template>

<script setup>
import { ref, onMounted, onUpdated, onUnmounted, onBeforeMount } from "vue";
import { useRouter } from "vue-router";
import { arrowBackOutLine } from "ionicons/icons";

const router = useRouter();
const name = ref("");
const address = ref();

const back = () => {
  router.back();
};
</script>

<style>
.padding {
  padding: 10px 5px;
}
</style>
