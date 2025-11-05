<script setup lang="ts">
import {VueDatePicker} from '@vuepic/vue-datepicker';
import '@vuepic/vue-datepicker/dist/main.css'

const modelValue = defineModel<string>();
</script>

<template>
  <VueDatePicker
      class="datepicker-primary"
      :model-value="modelValue"
      :inline="true"
      :day-names="['Пн', 'Вт', 'Ср', 'Чт', 'Пт', 'Сб', 'Вс']"
      :auto-apply="true"
      :enable-time-picker="false"
      :ui="{
      calendar: 'dp-custom-calendar',
      menu: 'dp-custom-menu',
    }"
  >
  </VueDatePicker>
</template>

<style lang="scss">
.dp__main {
  padding: 25px 20px;
}

/* Главный экран календаря */
.dp__theme_light {
  border: none;
  box-shadow: 0 8px 12px 0 rgba(91, 98, 139, 0.08);
  border-radius: 12px;
  background: #ffffff;
}

.dp__calendar_header_item {
  font-weight: 400;
  font-size: 12px;
  line-height: 133%;
  color: #787878;
}

.dp__month_year_select {
  font-weight: 700 !important;
  font-size: 18px !important;
  line-height: 111% !important;
}

.dp--header-wrap {
  margin-bottom: 50px;
}

/* Контейнер для айтемов */
.dp__calendar_item {
  text-align: -webkit-center;
}

/* Основные стили календаря */
.datepicker-primary {
  --dp-cell-size: 40px;
  --dp-border-radius: 8px;
  --dp-font-family: 'Inter', sans-serif;
}

.dp-custom-calendar {
  border: none;
  box-shadow: none;
  width: 100%;
}

.dp-custom-menu {
  box-shadow: none;
}

/* Стили для заголовка */
.dp__month_year_row {
  padding: 0 0 16px 0;
}

.dp__month_year_select {
  font-weight: 500;
  font-size: 16px;
  line-height: 24px;
  color: #1a1a1a;
}

/* Стили дней недели */
.dp__weekday {
  color: #808080;
  font-size: 14px;
  font-weight: 400;
  padding-bottom: 8px;
}

/* Стили ячеек дней */
.dp__cell {
  border-radius: 8px;
}

.dp__cell_inner {
  font-size: 14px;
  font-weight: 400;
  color: #1a1a1a;
}

.dp__today {
  border: 1px solid #5972fd;
  border-radius: 50%;
}

.dp__active_date {
  background: #5972fd;
  border-radius: 50%;
  color: white;
}

.dp__active_date .dp__cell_inner {
  color: white;
}

.dp__cell_inner:hover {
  background: #5972fd;
  opacity: 0.8;
  border-radius: 50%;
  color: white;
}

/* Стили для индикаторов событий */
.dp__cell .dp__dot {
  width: 6px;
  height: 6px;
  bottom: 4px;
}
.day-container {
  display: flex;
  flex-direction: column;
  align-items: center;
  gap: 2px;
}

.markers-container {
  display: flex;
  gap: 2px;
  justify-content: center;
}

.marker {
  width: 6px;
  height: 6px;
  border-radius: 50%;
}
</style>

