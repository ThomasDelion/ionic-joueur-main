<template>
  <ion-page>
    <ion-tabs>
      <ion-router-outlet></ion-router-outlet>



    </ion-tabs>
  </ion-page>
</template>

<script>
import { defineComponent } from 'vue';
import { IonTabs, IonPage, IonRouterOutlet } from '@ionic/vue';
import { ellipse, square, triangle } from 'ionicons/icons';

export default defineComponent({
  name: 'TabsPage',
  components: { IonTabs, IonPage, IonRouterOutlet },
  setup() {
    return {
      ellipse,
      square,
      triangle,
    }
  }
});
</script>