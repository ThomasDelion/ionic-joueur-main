<template>
  <div id="usercard">
    <p>ㅤ{{ name }}ㅤ</p>
      <ion-button class="btn9" color="danger" shape="round" @click="decrement()">-</ion-button>
      <p>ㅤ{{ score }}ㅤ</p>
      <ion-button class="btn9" color="primary" shape="round" @click="increment()">+</ion-button>
  </div>
</template>

<script>
import {defineComponent, ref} from "vue";
import {IonButton, } from "@ionic/vue";

export default defineComponent({
  name: "UserCard.vue",
  components: { IonButton, },
  props: {
    name: String,
    score: Number
  },

  setup() {
    let score = ref(0)

    const decrement = () => {
      score.value--
    }

    const increment = () => {
      score.value++
    }

    // eslint-disable-next-line vue/no-dupe-keys
    return {score, decrement, increment}
  }
});

</script>

<style scoped lang="scss">
#usercard {
  border: 1px solid black;
  border-radius: 5px;
  display: flex;
}

.btn9 {
  margin-left: 10px;
}

</style>