<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title class="ion_center">Commander</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 2</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-item>
        <ion-label position="floating" class="ion_center">Produit</ion-label>
        <ion-input type="text" v-model="name" class="ion_center"></ion-input>
      </ion-item>
      <ion-button color="primary" @click="addUser" shape="round" class="ion-activatable ripple-parent custom-parent">Ajouter</ion-button>

      <div id="list__produit">
        <user-card v-for="(user, index) in users" :key="index" :name="user.name" :score="1" class="ion_center"/>
      </div>
      <br>
      <ion-button color="warning" @click="Validate" shape="round" fill="outline" class="ion-activatable ripple-parent_bis custom-parent">Valider</ion-button>
      <ion-button color="warning" @click="resetUser" href="/tabs/tab1" shape="round" fill="outline" class="ion-activatable ripple-parent_bis custom-parent">Annuler</ion-button>
      <br>
    </ion-content>
  </ion-page>
</template>
<script>
import {defineComponent, ref} from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonItem, IonLabel, IonInput, IonButton} from '@ionic/vue';
import UserCard from "@/components/UserCard";

export default defineComponent({
  name: 'Tab2Page',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonItem, IonLabel, IonInput, IonButton, UserCard},
  setup() {
    let users = ref([])
    let name = ref('')

    const addUser = () => {
      users.value.push({
        name: name.value,
      })
      name.value = ''
    }
    const resetUser = () => {
      users.value = []
    }
    const Validate = () => {
      this.buttonColor = '#345465';
    }


    return {users, name, addUser, resetUser, Validate}
  }
});
</script>
