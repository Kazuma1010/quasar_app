<template>
  <q-page class="about-title">
    <div>
      <q-select outlined v-model="model" :options="options" label="Outlined" />
    </div>
  </q-page>
</template>

<style lang="scss">
.about-title {
  color: black;
}
</style>

<script>
export default {
  name: 'PageAbout',
  data () {
    return {
      model: null,
      options: [
        'Google', 'Facebook', 'Twitter', 'Apple', 'Oracle'
      ]
    }
  }
}
</script>
