<template>
  <q-expansion-item
    clickable
    tag="a"
    target="_blank"
    :label="title"
  >

    <div
    >
      <q-item
        :to="link"
      >
        <q-item-section
          v-if="icon"
          avatar
        >
          <q-icon :name="icon" />
        </q-item-section>

        <q-item-section>
          <q-item-label>{{ title }}</q-item-label>
        </q-item-section>

      </q-item>

    </div>
  </q-expansion-item>
</template>

<script>
export default {
  name: 'EssentialLink',

  props: {
    id: {
      type: Number,
      required: true
    },
    icon: {
      type: String,
      default: ''
    },
    title: {
      type: String,
      required: true
    },
    link: {
      type: String,
      default: '#'
    }
    // subTitle: {
    //   type: Array,
    //   default: () => [
    //     {
    //       id: {
    //         type: Number,
    //         required: true
    //       },
    //       icon: {
    //         type: String,
    //         default: ''
    //       },
    //       name: {
    //         type: String,
    //         required: true
    //       },
    //       link: {
    //         type: String,
    //         default: '#'
    //       }
    //     }
    //   ]
    // }
  }
}
</script>
