<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title class="ion_center">Connexion</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-item>
        <ion-label position="floating" class="ion_center">Email</ion-label>
        <ion-input type="text" v-model="Email" class="ion_center"></ion-input>
        <ion-label position="floating" class="ion_center">Mot de passe</ion-label>
        <ion-input type="text" v-model="Password" class="ion_center"></ion-input>
      </ion-item>
      <ion-button color="primary" @click="connexion" class="ion_center center_buton"  shape="round">Connexion</ion-button>
    </ion-content>
  </ion-page>
</template>

<script>
import {defineComponent} from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonItem, IonLabel, IonInput, IonButton } from '@ionic/vue';

export default defineComponent({
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonItem, IonLabel, IonInput, IonButton},
  setup() {


  }
})
</script>

