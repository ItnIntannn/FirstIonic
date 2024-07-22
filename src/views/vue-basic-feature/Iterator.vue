import { arrowBackOutline } from 'ionicons/icons';
<template>
  <ion-page>
    <ion-header>
      <ion-toolbar color="primary">
        <ion-buttons slot="start">
          <ion-button @click="back">
            <ion-icon slot="icon-only" :icon="arrowBackOutline"></ion-icon>
          </ion-button>
        </ion-buttons>
        <ion-title>Itelator</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Itelator</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-list>
        <ion-list-header>Itelator dengan variable biasa</ion-list-header>

        <ion-item v-for="item in contacts">
          <ion-label>
            <h2>{{ item.nama }}</h2>
            <p>{{ item.phone }}</p>
            <p>{{ item.email }}</p>
          </ion-label>
        </ion-item>
      </ion-list>

      <ion-list>
        <ion-list-header>Iterator dengan variable ref</ion-list-header>

        <ion-item v-for="item in contactRefs">
          <ion-label>
            <h2>{{ item.nama }}</h2>
            <p>{{ item.phone }}</p>
            <p>{{ item.email }}</p>
          </ion-label>
        </ion-item>
      </ion-list>
    </ion-content>
  </ion-page>
</template>

<script setup>
import { ref } from "vue";
import { useRouter } from "vue-router";
import { arrowBackOutline } from "ionicons/icons";

const router = useRouter();

const back = () => {
  router.back();
};

const contacts = [
  {
    nama: "Intan",
    phone: "085606245238",
    email: "intanaini280405@gmail.com",
  },
  {
    nama: "Annura",
    phone: "08567436381",
    email: "annuraaa@gmail.com",
  },
  {
    nama: "Intanna",
    phone: "08963358389",
    email: "IntannaIn@gmail.com",
  },
];

const contactRefs = ref([
  {
    nama: "Intan",
    phone: "085606245238",
    email: "intanaini280405@gmail.com",
  },
  {
    nama: "Annura",
    phone: "08567436381",
    email: "annuraaa@gmail.com",
  },
  {
    nama: "Intanna",
    phone: "08963358389",
    email: "IntannaIn@gmail.com",
  },
]);
</script>

<style></style>
