<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Tab 4</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 4</ion-title>
        </ion-toolbar>
      </ion-header>
        <h2>Véhicules</h2>
        <div class="block_vehicule">
          <div class="list_vehicule">
            <button>Véhicule 1</button>
          </div>
        </div>
    </ion-content>
  </ion-page>


</template>

<script>
import { defineComponent } from 'vue';
import { IonHeader, IonToolbar, IonTitle, IonContent , IonPage} from '@ionic/vue';

export default defineComponent({
  name: 'Tab4Page',
  components: {IonHeader, IonToolbar, IonTitle, IonContent, IonPage },

});
</script>
<style scoped>
  button{
    background: #2fdf75;
  }
</style>