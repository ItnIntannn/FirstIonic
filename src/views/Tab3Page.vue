<template>
  <ion-page>
    <ion-header>
      <ion-toolbar color="primary">
        <ion-title>Setting Latihan</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Latihan</ion-title>
        </ion-toolbar>
      </ion-header>

      <!-- <p>{{ name }}</p>
      <h2>{{ kelas }}</h2> -->

      <ion-list>
        <ion-list-header>Vue Basic Feature</ion-list-header>

        <ion-item @click="toState" class="ion-activatable ripple-parent">
          <ion-ripple-effect></ion-ripple-effect>
          <ion-label>
            <h2>State</h2>
            <p>State Management?</p>
          </ion-label>
        </ion-item>

        <ion-item @click="toIterator" class="ion-activatable ripple-parent">
          <ion-ripple-effect></ion-ripple-effect>
          <ion-label>
            <h2>Iterator - v-for</h2>
            <p></p>
          </ion-label>
        </ion-item>

        <ion-item @click="toModal" class="ion-activatable ripple-parent">
          <ion-ripple-effect></ion-ripple-effect>
          <ion-label>
            <h2>Model - Two Data Binding - v-if</h2>
            <p></p>
          </ion-label>
        </ion-item>

        <ion-item @click="toEvent" class="ion-activatable ripple-parent">
          <ion-ripple-effect></ion-ripple-effect>
          <ion-label>
            <h2>Event</h2>
            <p></p>
          </ion-label>
        </ion-item>

        <ion-item @click="toLifecycle" class="ion-activatable ripple-parent">
          <ion-ripple-effect></ion-ripple-effect>
          <ion-label>
            <h2>Lifecycle</h2>
            <p></p>
          </ion-label>
        </ion-item>
      </ion-list>
    </ion-content>
  </ion-page>
</template>

<script setup lang="ts">
import { useRouter } from "vue-router";

const router = useRouter();

const toEvent = () => router.push({ path: "/vue/event" });
const toIF = () => router.push({ path: "/vue/IF" });
const toIterator = () => router.push({ path: "/vue/iterator" });
const toLifecycle = () => router.push({ path: "/vue/lifecycle" });
const toModal = () => router.push({ path: "/vue/modal" });
const toState = () => router.push({ path: "/vue/state" });

// VARIABEL let, var, const
// penulisan variabel dengan const
// let tidak bersifat constatnt. jadi nilai variabel bisa dirubah
let name = "intan";

// penulisan variabel dengan const
// const bersifat constatnt. jadi nilai variabel tidak bisa dirubah
const kelas = "ik2";

// FUNCTION
// menggunakan syntax function
const gantiNama = (name: string) => {
  alert("ganti nama");
};

// menggunakan syntax coust
const gantiKelas = (name: string) => {
  alert("ganti kelas");
};

// TIPE PRIMITIVE
// string, number, boolean, any, Array
// 1. string
const peliharaan: string = "pig";

// 2. number
const umur: number = 10.5;

// 3. boolean
const isHidup: boolean = false; // true, false

// 4. any
const gakjelas: any = false;

// 5. Array
const names: Array<string> = ["intan", "anura", "intanna", "pig"];

const nilais: number[] = [123, 10, 20, 30];

const semrawut: any[] = ["aku", 123, true];

// TIPE DATA OBJECT
const orang = {
  nama: "intan",
  kelas: "ik2",
  umur: 18,
  pacars: ["hwhwbks", "swojsk"],

  ayah: {
    nama: "Wiyono",
    jk: 1,
    alamat: "Sidokare,Rejoso,Nganjuk",
  },
  ibu: {
    nama: "Kartini",
    jk: 2,
    alamat: "Sidokare,Rejoso,Nganjuk",
  },
};

// TYPE -enumable
type KELAMIN = "laki-laki" | "perempuan";
</script>
