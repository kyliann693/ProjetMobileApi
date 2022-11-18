<template>
  <ion-page id="background_header">
    <ion-header>
      <ion-toolbar>
        <ion-title class="title_tab_1 ion_center">Inscription</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 2</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-item>
        <ion-label position="floating" class="ion_center">Email</ion-label>
        <ion-input type="text" v-model="email" class="ion_center"></ion-input>
        <ion-label position="floating" class="ion_center">Mot de passe</ion-label>
        <ion-input type="text" v-model="password_retype" class="ion_center"></ion-input>
        <ion-label position="floating" class="ion_center">Comfirmation du Mot de passe</ion-label>
        <ion-input type="text" v-model="password" class="ion_center"></ion-input>
      </ion-item>
      <ion-button color="primary" @click="addUser" class="ion_center center_buton"  shape="round">S'inscrire</ion-button>

    </ion-content>
  </ion-page>
</template>
<script>
import {defineComponent} from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonItem, IonLabel, IonInput, IonButton } from '@ionic/vue';


export default defineComponent({
  name: 'Tab2Page',
  components: {IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonItem, IonLabel, IonInput, IonButton}
});
</script>
