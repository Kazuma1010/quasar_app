<template>
  <q-page class="entry">
    <div class="row-12">
      <q-card>
        <q-card-section>
          <div class="text-h5 bg-primary text-white entry-title">Entry</div>
        </q-card-section>
      </q-card>
    </div>
    <div class="row">
      <div class="col-3">
        <q-card>
          <q-card-section>
            <div class="text-h6 entry-label">Main Label</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-9">
        <q-card>
          <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Sub Label" />
          </q-card-section>
          <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Sub Label" />
          </q-card-section>
          <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Sub Label" />
          </q-card-section>
           <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Sub Label" />
          </q-card-section>
           <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Sub Label" />
          </q-card-section>
        </q-card>
      </div>
    </div>
    <div class="row">
      <div class="col-3">
        <q-card>
          <q-card-section>
            <div class="text-h6 entry-label">Main Label</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-3">
        <q-card>
          <q-card-section>
            <div class="text-h6 entry-label">Sub Label</div>
          </q-card-section>
          <q-card-section>
            <div class="text-h6 entry-label">Sub Label</div>
          </q-card-section>
          <q-card-section>
            <div class="text-h6 entry-label">Sub Label</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-6">
        <q-card>
          <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Outlined" />
          </q-card-section>
          <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Outlined" />
          </q-card-section>
          <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Outlined" />
          </q-card-section>
        </q-card>
      </div>
    </div>
    <div class="row">
      <div class="col-3">
        <q-card>
          <q-card-section>
            <div class="text-h6 entry-label">Main Label</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-3">
        <q-card>
          <q-card-section>
            <div class="text-h6 entry-label">Sub Label</div>
          </q-card-section>
          <q-card-section>
            <div class="text-h6 entry-label">Sub Label</div>
          </q-card-section>
        </q-card>
      </div>
      <div class="col-6">
        <q-card>
          <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Outlined" />
          </q-card-section>
          <q-card-section>
            <q-select outlined v-model="model" :options="options" label="Outlined" />
          </q-card-section>
        </q-card>
      </div>
    </div>
    <div class="row justify-between">
      <q-btn
        push
        size="md"
        color="secondary"
        label="Import"
        v-close-popup
      />
      <q-btn
        push
        size="md"
        color="secondary"
        label="Submit"
        v-close-popup
      />
    </div>
  </q-page>
</template>

<style lang="scss">
.entry{
  .entry-title {
    padding: 0.5em;
  }

  .entry-label {
    padding: 0.6em;
  }
}
</style>

<script>
export default {
  name: 'PageEntry',
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