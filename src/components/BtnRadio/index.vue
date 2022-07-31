<template>
  <!-- <div class="wrapper">
    <radio-btn
      v-for="(item, index) of subjects"
      :key="index"
      :indexx="index"
      :curIdx="curIdx"
      :item="item"
      @radioCheck="radioCheck"
    />
  </div> -->
  <!-- 事件代理方式 -->
  <div class="wrapper" @click="radioCheckEvent($event)">
    <radio-btn-event
      v-for="(item, index) of subjects"
      :key="index"
      :indexx="index"
      :curIdx="curIdx"
      :item="item"
    />
  </div>
</template>
<script>
import RadioBtn from "./Button";
import RadioBtnEvent from "./ButtonEvent";
export default {
  name: "BtnRadio",
  props: {
    subjects: Array,
  },
  components: {
    RadioBtn,
    RadioBtnEvent,
  },
  data() {
    return {
      curIdx: 0,
    };
  },
  methods: {
    radioCheck(index) {
      this.curIdx = index;
    },
    radioCheckEvent(e) {
      console.log(e.target);
      const tar = e.target;
      const className = tar.className;
      if (className === "radio-btn") {
        const index = Number(tar.dataset.index);
        this.curIdx = index;
      }
    },
  },
};
</script>