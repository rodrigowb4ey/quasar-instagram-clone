<template>
  <q-page class="constrain q-pa-md">

    <div class="row q-col-gutter-lg">
      <div class="col-12 col-sm-8">
        <q-card
          v-for="post in posts"
          :key="post.id"
          class="card-post q-mb-md"
          flat
          bordered>
          <q-item>
            <q-item-section avatar>
              <q-avatar>
                <img src="https://pbs.twimg.com/profile_images/1371630348556177411/H-KKwOtH_400x400.jpg">
              </q-avatar>
            </q-item-section>

            <q-item-section>
              <q-item-label class="text-bold">@armin_arlet</q-item-label>
              <q-item-label caption>
                {{ post.location }}
              </q-item-label>
            </q-item-section>
          </q-item>

          <q-separator />

          <q-img
            :src="post.imageUrl"
          />
          <q-card-section>
            <div class="">{{ post.caption }}</div>
            <div class="text-caption text-grey">{{ niceDate(post.date) }}</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-4 large-screen-only">
        <q-item class="fixed">
          <q-item-section avatar>
            <q-avatar size="48px">
              <img src="https://pbs.twimg.com/profile_images/1371630348556177411/H-KKwOtH_400x400.jpg">
            </q-avatar>
          </q-item-section>

          <q-item-section>
            <q-item-label class="text-bold">@armin_arlet</q-item-label>
            <q-item-label caption>
              Armin Arlet
            </q-item-label>
          </q-item-section>
        </q-item>
      </div>
    </div>

    <q-card
      v-for="post in posts"
      :key="post.id"
      class="card-post q-mb-md"
      flat
      bordered>
      <q-item>
        <q-item-section avatar>
          <q-avatar>
            <img src="https://pbs.twimg.com/profile_images/1371630348556177411/H-KKwOtH_400x400.jpg">
          </q-avatar>
        </q-item-section>

        <q-item-section>
          <q-item-label class="text-bold">@armin_arlet</q-item-label>
          <q-item-label caption>
            {{ post.location }}
          </q-item-label>
        </q-item-section>
      </q-item>

      <q-separator />

      <q-img
        :src="post.imageUrl"
      />
      <q-card-section>
        <div class="">{{ post.caption }}</div>
        <div class="text-caption text-grey">{{ niceDate(post.date) }}</div>
      </q-card-section>
    </q-card>
  </q-page>
</template>

<script>
import { date } from 'quasar'

export default {
  name: 'PageHome',
  data() {
    return {
      posts: [
        {
          id: 1,
          caption: 'Have you ever seen the ocean?',
          date: 1642427408372,
          location: 'Shiganshina Distric, Paradis Island',
          imageUrl: 'https://i.pinimg.com/originals/a7/57/a7/a757a7e3c7cd29073a24cee6b4a84f9c.jpg',
        },
        {
          id: 2,
          caption: 'Have you ever seen the ocean?',
          date: 1642427408372,
          location: 'Shiganshina Distric, Paradis Island',
          imageUrl: 'https://i.pinimg.com/originals/a7/57/a7/a757a7e3c7cd29073a24cee6b4a84f9c.jpg',
        },
        {
          id: 3,
          caption: 'Have you ever seen the ocean?',
          date: 1642427408372,
          location: 'Shiganshina Distric, Paradis Island',
          imageUrl: 'https://i.pinimg.com/originals/a7/57/a7/a757a7e3c7cd29073a24cee6b4a84f9c.jpg',
        },
        {
          id: 4,
          caption: 'Have you ever seen the ocean?',
          date: 1642427408372,
          location: 'Shiganshina Distric, Paradis Island',
          imageUrl: 'https://i.pinimg.com/originals/a7/57/a7/a757a7e3c7cd29073a24cee6b4a84f9c.jpg',
        }
      ]
    }
  },
  methods: {
    niceDate(value) {
      return date.formatDate(value, 'MMMM D h:mmA')
    }
  }
}
</script>

<style lang="sass">
  .card-post
    .q-image
      min-height: 200px
</style>
