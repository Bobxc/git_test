<template>
  <button
    :class="['radio-btn', { current: indexx === curIdx }]"
    :data-index="indexx"
  >
    {{ item }}
  </button>
</template>
<script>
export default {
  name: "RadioBtn",
  props: {
    item: String,
    indexx: Number,
    curIdx: Number,
  },
  methods: {},
};
</script>
<style lang="scss" scoped>
.radio-btn {
  height: 34px;
  border: none;
  outline: none;
  padding: 0 15px;
  margin-right: 20px;
  border-radius: 5px;
  border-radius: 5px;
  color: #999;
  border: 1px solid #ddd;
  background-color: #eee;
}
.radio-btn.current {
  background-color: #fff;
  color: red;
  border-color: red;
}
</style>