<template>
  <div class="wrapper">
    <Datepicker v-model="data.date" :lang="data.lang"></Datepicker>
    <div class="item">
      <label>Выберите язык:</label>
      <select v-model="data.lang">
        <option :value="'ru'">Русский</option>
        <option :value="'en'">Английский</option>
      </select>
    </div>
  </div>
</template>

<script>
import "vue-datepicker-ui/lib/vuedatepickerui.css";
import VueDatepickerUi from "vue-datepicker-ui";

export default {
  components: {
    Datepicker: VueDatepickerUi,
  },
  data: function () {
    return {
      data: {
        date: new Date(),
        lang: "ru",
      },
    };
  },
};
</script>

<style scoped>
.wrapper {
  display: flex;
  gap: 1rem;
}
.item {
  display: flex;
  flex-direction: column;
  gap: 0.5rem;
}
</style>
