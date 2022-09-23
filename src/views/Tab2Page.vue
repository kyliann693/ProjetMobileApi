<!--Réaliser par Kyliann Aland et Alexis Rossignol-->
<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Partie</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Tab 2</ion-title>
        </ion-toolbar>
      </ion-header>

      <ion-item>
        <ion-label position="floating">Nom utilisateur</ion-label>
        <ion-input type="text" v-model="name"></ion-input>
      </ion-item>
      <ion-button color="primary" @click="addUser">Ajouter</ion-button>

      <div id="list__users">
        <user-card v-for="(user, index) in users" :key="index" :name="user.name" :score="number"/>
      </div>
      <ion-button color="danger" @click="decrement()">-</ion-button>
      <span></span>
      <ion-button color="primary" @click="increment()">+</ion-button>
      <br>
      <ion-button color="warning" @click="resetUser">Réinitialiser</ion-button>
      <ion-button color="warning" @click="resetUser" href="/tabs/tab1">Arret</ion-button>
      <br>
    </ion-content>
  </ion-page>
</template>
<script>
import {defineComponent, ref} from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonItem, IonLabel, IonInput, IonButton } from '@ionic/vue';
import UserCard from "@/components/UserCard";

export default defineComponent({
  name: 'Tab2Page',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonItem, IonLabel, IonInput, IonButton, UserCard },
  setup() {
    let users = ref([])
    let name = ref('')
    let number = ref(0)

    const addUser = () => {
      users.value.push({
        name: name.value,
        score: 0
      })
      name.value = ''
    }
    const resetUser = () => {
      users.value = []
    }
    const decrement = () => {
      number.value--
    }

    const increment = () => {
      number.value++
    }

    return {users, name, addUser, resetUser, number, decrement, increment}
  }
});
</script>
