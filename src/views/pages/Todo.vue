<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Todo Apps</ion-title>
      </ion-toolbar>
    </ion-header>

    <ion-content :fullscreen="true">
      <ion-list>
        <ion-list-header>
          <ion-label>MUSEUM ANURA</ion-label>
        </ion-list-header>

        <ion-item>
          <ion-label>
            <h2>Lukisan</h2>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit.</p>
          </ion-label>
        </ion-item>

        <ion-item>
          <ion-label>
            <h2>Artifacts</h2>
            <p>
              Lorem ipsum, dolor sit amet consectetur adipisicing elit. Quaerat est et
              consectetur? Porro, earum expedita voluptatem totam odio quasi autem iure
              nam sed, obcaecati maxime a provident neque dignissimos consequatur?
            </p>
          </ion-label>
        </ion-item>

        <ion-item>
          <ion-label>
            <h2>Exhibit(Pemeran)</h2>
            <p>
              Lorem ipsum dolor sit amet, consectetur adipisicing elit. Fugit, suscipit
              quisquam amet dignissimos labore quibusdam voluptatibus beatae unde voluptas
              ab sapiente, obcaecati eos officia voluptatum dicta? Sit ab doloribus sed!
            </p>
          </ion-label>
        </ion-item>

        <ion-item>
          <ion-label>
            <h2>Information (Informasi)</h2>
            <p>
              Lorem ipsum dolor, sit amet consectetur adipisicing elit. Dolorum sequi enim
              repudiandae laboriosam facilis repellendus iste ipsa alias exercitationem
              iure quos quidem, ullam assumenda, incidunt ducimus autem provident, eius
              soluta!
            </p>
          </ion-label>
        </ion-item>
      </ion-list>

      <!-- <ion-button expand="full" fill="outline" color="danger">Default</ion-button>
      <ion-button color="warning" :disable="true">Disable</ion-button> -->

      <ion-fab slot="fixed" horizontal="end" vertical="button">
        <ion-fab-button color="success">
          <ion-icon :icon="add"></ion-icon>
        </ion-fab-button>
      </ion-fab>
    </ion-content>
  </ion-page>
</template>

<script setup>
import { logoIonic, add } from "ionicons/icons";
</script>

<style>
ion-content {
  height: 90%;
}
</style>
