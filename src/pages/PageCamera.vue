<template>
  <q-page class="constrain-more q-pa-md">
    <div class="camera-frame q-pa-md">
      <img
        class="full-width"
        src="https://i.pinimg.com/originals/a7/57/a7/a757a7e3c7cd29073a24cee6b4a84f9c.jpg">
    </div>
    <div class="text-center q-pa-md">
      <q-btn
        size="lg"
        round
        color="grey-10"
        icon="eva-camera"
      />
      <div class="row justify-center q-ma-md">
        <q-input
          v-model="post.caption"
          label="Caption"
          class="col col-sm-6"
          dense
        />
      </div>
      <div class="row justify-center q-ma-md">
        <q-input
          v-model="post.location"
          label="Location"
          class="col col-sm-6"
          dense
        >
          <template v-slot:append>
            <q-btn round dense flat icon="eva-navigation-2-outline" />
          </template>
        </q-input>
      </div>
      <div class="row justify-center q-mt-lg">
        <q-btn
          unelevated
          rounded
          color="primary"
          label="Post Image" />
      </div>
    </div>
  </q-page>
</template>

<script>
import { uid } from 'quasar'

export default{
  name: 'PageCamera',
  data() {
    return {
      post: {
        id: uid(),
        caption: '',
        location: '',
        photo: null,
        date: Date.now(),
      }
    }
  }
}
</script>

<style lang="sass">
.camera-frame
  border: 2px solid $grey-10
  border-radius: 10px
</style>
