<template>
  <div class="home">
    <btn-radio :subjects="subjects" />
  </div>
</template>

<script>
import BtnRadio from "@/components/BtnRadio";
export default {
  name: "Home",
  components: {
    BtnRadio,
  },
  data() {
    return {
      subjects: ["vue", "react", "angular"],
    };
  },
};
</script>
<style lang="scss" scoped>
.home {
  margin: 0;
  padding: 0;
}
</style>
