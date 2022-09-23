<template>
  <ion-page>
    <ion-header>
      <ion-toolbar>
        <ion-title>Calculateur de points</ion-title>
      </ion-toolbar>
    </ion-header>
    <ion-content :fullscreen="true">
      <ion-header collapse="condense">
        <ion-toolbar>
          <ion-title size="large">Calculateur de point</ion-title>
        </ion-toolbar>
      </ion-header>


      <ion-item>
        <ion-label position="floating">Nom de la partie</ion-label>
        <ion-input type="text" v-model="Name_Partie"></ion-input>
      </ion-item>
      <ion-button color="primary" router-link="/Tab2Page" >Nouvelle Partie</ion-button>



    </ion-content>
  </ion-page>
</template>

<script>
import {defineComponent, ref} from 'vue';
import { IonPage, IonHeader, IonToolbar, IonTitle, IonContent, IonItem, IonLabel, IonInput, IonButton } from '@ionic/vue';

export default defineComponent({
  name: 'Tab1Page',
  components: { IonHeader, IonToolbar, IonTitle, IonContent, IonPage, IonItem, IonLabel, IonInput, IonButton,},
  setup() {

    let Name_Partie = ref('')

    return {Name_Partie}
  }
});
</script>