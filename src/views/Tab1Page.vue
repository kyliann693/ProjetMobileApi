<!--Réaliser par Kyliann Aland et Alexis Rossignol-->
<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Création de partie</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 1</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-item>
        <ion-label position="floating">Nom de la partie</ion-label>
        <ion-input type="text" v-model="party_name"></ion-input>
      </ion-item>
      <ion-button color="primary" @click="addParty" href="/tabs/tab2">Ajouter une partie</ion-button>
    </ion-content>
  </ion-page>
</template>

<script>
import {defineComponent} from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonItem, IonLabel, IonInput, IonButton } from '@ionic/vue';

export default defineComponent({
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonItem, IonLabel, IonInput, IonButton},
  setup() {

    // function addParty () {
    //   this.$router.push("tabs2")
    //
    // }
    // return {addParty}
  }
})
</script>