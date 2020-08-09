<template>
  <q-page class="list">
    <div class="row-12">
      <q-card>
        <q-card-section>
          <div class="text-h5 bg-brimary text-white list-title">list</div>
        </q-card-section>
      </q-card>
    </div>
    <div class="row-12">
      <div class="col-6">
        <q-card>
          <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Label" />
          </q-card-section>
        </q-card>
      </div>
      <div class="col-6">
        <q-card>
          <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Label" />
          </q-card-section>
        </q-card>
      </div>
    </div>
  </q-page>
</template>

<style lang="scss">
.list {
  .list-title {
    padding: 0.5em;
  }
}
</style>

<script>
export default {
  name: 'PageList',
  data() {
    return {
      model: null,
      options: [
        'Google', 'Facebook', 'Twitter', 'Apple', 'Oracle'
      ]
    }
  }
}
</script>