<template>
  <q-layout view="lHh Lpr lFf">
    <q-header elevated>
      <q-toolbar>
        <q-btn
          flat
          dense
          round
          icon="menu"
          aria-label="Menu"
          @click="leftDrawerOpen = !leftDrawerOpen"
        />

        <q-toolbar-title>
          LOGO
        </q-toolbar-title>

        <!-- <div>Quasar v{{ $q.version }}</div> -->
        <div class="q-pa-md">
        <q-btn-dropdown
          flat
          color="white"
          label="User name"
          icon="person"
          class="profile-button"
        >
          <div class="row no-wrap q-pa-md justify-center">

            <div class="column items-center">
              <q-avatar size="72px">
                <q-icon name="person" />
              </q-avatar>

              <div class="text-subtitle1 q-mt-md q-mb-xs">User name</div>

              <q-btn
                color="primary"
                label="Logout"
                push
                size="md"
                v-close-popup
              />
            </div>
          </div>
        </q-btn-dropdown>
            </div>

      </q-toolbar>
    </q-header>

    <q-drawer
      v-model="leftDrawerOpen"
      show-if-above
      bordered
      content-class="bg-grey-1"

      :mini="miniState"
      @mouseover="miniState = false"
      @mouseout="miniState = true"
    >
      <q-list>
        <q-item>
          <q-item-section avatar>
            <q-icon name="person" />
          </q-item-section>
          <q-item-section>
            <q-item-label
              class="text-grey-8"
            >
              Menu
            </q-item-label>
          </q-item-section>
        </q-item>
        <q-item
          to="/"
          class="text-black"
        >
          <q-item-section avatar>
            <q-icon name="home" />
          </q-item-section>
          <q-item-section>
            <q-item-label>
              Home
            </q-item-label>
          </q-item-section>
        </q-item>

        <EssentialLink
          v-for="link in essentialLinks"
          :key="link.id"
          v-bind="link"
        />
      </q-list>
    </q-drawer>

    <q-page-container>
      <router-view />
    </q-page-container>
  </q-layout>
</template>

<style lang="scss">
.profile-button {
  border: none;
}
</style>

<script>
import EssentialLink from 'components/EssentialLink.vue'

const linksData = [
  {
    id: 1,
    icon: 'create',
    title: 'Entry',
    link: '/entry'
    // subTitle: [
    //   {
    //     id: 1,
    //     icon: 'person',
    //     name: 'Entry',
    //     link: '/entry'
    //   },
    //   {
    //     id: 2,
    //     icon: 'person',
    //     name: 'List',
    //     link: '/Index'
    //   }
    // ]
  },
  {
    id: 2,
    icon: 'menu_book',
    title: 'List',
    link: '/list'
  },
  {
    id: 3,
    title: 'Github',
    icon: 'code',
    link: 'https://github.com/quasarframework'
  },
  {
    id: 4,
    title: 'Discord Chat Channel',
    icon: 'chat',
    link: 'https://chat.quasar.dev'
  },
  {
    id: 5,
    title: 'Forum',
    icon: 'record_voice_over',
    link: 'https://forum.quasar.dev'
  }
  // {
  //   title: 'Twitter',
  //   icon: 'rss_feed',
  //   link: 'https://twitter.quasar.dev'
  // },
  // {
  //   title: 'Facebook',
  //   icon: 'public',
  //   link: 'https://facebook.quasar.dev'
  // },
  // {
  //   title: 'Quasar Awesome',
  //   icon: 'favorite',
  //   link: 'https://awesome.quasar.dev'
  // }
]

export default {
  name: 'MainLayout',
  components: { EssentialLink },
  data () {
    return {
      miniState: true,
      leftDrawerOpen: false,
      essentialLinks: linksData,
      options: [
        'Logout'
      ]
    }
  }
}
</script>
