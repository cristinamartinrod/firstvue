<template>
  <section class="project">
    <div class="image"></div>
    <div class="textContent">
      <div class="header-box">
        <h4 v-if="!editing" class="title">{{ title }}</h4>
        <input v-if="editing" v-model="title" class="title inputStyle">
        <div class="btns">
          <span @click="onRemove">
            <i class="fas fa-times"></i>
          </span>
          <span>
            <i @click="edit" class="fas fa-pencil-alt"></i>
          </span>
        </div>
      </div>
      <p v-if="!editing" class="text">{{ text }}</p>
      <input v-if="editing" v-model="text" class="text inputStyle">
    </div>
  </section>
</template>

<script>
export default {
  name: "project",
  props: ["title", "text", "id"],
  mounted() {},
  data() {
    return {};
  },
  methods: {
    onRemove(event) {
      this.$emit("remove", this.id);
    }
  },
  computed: {}
};
</script>