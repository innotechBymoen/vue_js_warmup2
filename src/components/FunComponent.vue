<template>
  <div>
    <button @click="change_color">CLICK ME!</button>
    <section>
      <p v-for="(secret, i) in secrets" :key="i" @click="make_text_pink">
        {{ secret }}
      </p>
    </section>
  </div>
</template>

<script>
export default {
  data() {
    return {
      secrets: [
        `Did you know that Vue was made by Evan Yue?`,
        `Did you know that Vue is one of the most liked frameworks as voted by developers`,
      ],
    };
  },

  methods: {
    change_color: function () {
      document.body[`style`][`backgroundColor`] = `gold`;
    },
    make_text_pink(details) {
      details[`target`][`style`][`color`] = `pink`;
    },
  },
};
</script>

<style scoped>
</style>