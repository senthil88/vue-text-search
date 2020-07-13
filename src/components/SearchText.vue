<template>
  <b-container>
    <b-row align-v="center" class="justify-content-center">
      <b-nav-form>
        <b-form-input size="sm" class="mr-sm-2" placeholder="Search" v-model="queries"></b-form-input>
        <file-reader @load="text = $event"></file-reader>
      </b-nav-form>
    </b-row>

    <b-row id="content">
      <text-highlight :queries="queries">{{ text }}</text-highlight>
    </b-row>
  </b-container>
</template>

<script>
import FileReader from "./FileReader";
import TextHighlight from "vue-text-highlight";

export default {
  name: "SearchText",
  data: () => ({ text: "", queries: "" }),
  components: {
    FileReader,
    TextHighlight
  }
};
</script>

<style scoped>
  .container, #content {
    margin-top: 30px;
  }
</style>