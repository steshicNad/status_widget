<template>
  <div class="flex flex-col w-[25.9vw] rounded-2xl h-[34.8vh] bg-[#30323D]">
    <div
      class="flex z-10 w-[25.9vw] rounded-t-2xl h-[3.8vh] gap-[0.83vw] bg-[#30323D] shadow-md shadow-[#272933]">
      <div class="flex ml-[1.04vw] items-center text-[1.6vh] uppercase text-[#00FF94]">
        Состояния
      </div>
      <div class="ml-[7.34vw] w-maxw flex items-center gap-[0.83vw]">
        <div class="flex items-center text-[0.92vh] text-[#D6EBFF]">Время начала</div>
        <div class="flex items-center">
          <img src="src/img/vector.svg" class="h-[1.8vh] w-[1px]" />
        </div>
        <div class="flex items-center text-[0.92vh] text-[#D6EBFF]">Время окончания</div>
      </div>
    </div>
    <div
      class="flex flex-col pb-[2.4vh] mt-[2.4vh] overflow-y-auto pb-10 rounded-b-2xl w-[25.9vw] h-[31vh] bg-[#30323D]">
      <!-- 1 строка (таких надо 5) -->

      <div class="flex flex-col ml-[1.04vw]" v-for="(item, index) in test" :key="item">
        <div class="flex items-center">
          <div
            v-if="item.state == 'working'"
            class="flex truncate w-[10vw] items-center text-[1.48vh] text-[#00FF94]">
            {{ item.condition }}
          </div>
          <div v-else class="flex truncate w-[10vw] items-center text-[1.48vh] text-[#D6EBFF]">
            {{ item.condition }}
          </div>
          <div class="flex ml-[2.76vw] gap-[0.83vw] text-[1.1vh] text-[#00FF94]">
            <div class="flex gap-[0.41vw]">
              <div class="flex items-center">{{ item.data1 }}</div>
              <div class="flex items-center">{{ item.time1 }}</div>
            </div>

            <div class="flex items-center">
              <img src="src/img/vector.svg" class="h-[1.8vh] w-[1px]" />
            </div>

            <div class="flex gap-[0.41vw]">
              <div class="flex items-center">{{ item.data2 }}</div>
              <div class="flex items-center">{{ item.time2 }}</div>
            </div>
          </div>
        </div>
        <hr
          v-if="index != datasize - 1"
          class="h-px my-[0.83vh] w-[23.9vw] bg-[#00C2FF] border-0" />
      </div>
    </div>
  </div>
</template>

<script setup>
  import { ref } from 'vue';

  defineProps({
    msg: {
      type: String,
      required: true,
    },
  });

  const test = ref([
    {
      condition: 'В работе',
      data1: '06.10.22',
      time1: '16:49',
      data2: '12.10.22',
      time2: '12:00',
      state: 'working',
    },
    {
      condition: 'Работа на ТТ',
      data1: '07.10.22',
      time1: '12:29',
      data2: '--------',
      time2: '',
      state: 'not working',
    },
    {
      condition: 'Температура норм',
      data1: '08.10.22',
      time1: '11:55',
      data2: '14.10.22',
      time2: '15:32',
      state: 'working',
    },
    {
      condition: 'Номинальные обороты',
      data1: '09.10.22',
      time1: '10:12',
      data2: '15.10.22',
      time2: '10:11',
      state: 'not working',
    },
    {
      condition: 'Расход топлива норм',
      data1: '10.10.22',
      time1: '15:25',
      data2: '16.10.22',
      time2: '13:55',
      state: 'working',
    },
    {
      condition: 'Номинальные обороты',
      data1: '09.10.22',
      time1: '10:12',
      data2: '15.10.22',
      time2: '10:11',
      state: 'not working',
    },
    {
      condition: 'Расход топлива норм',
      data1: '10.10.22',
      time1: '15:25',
      data2: '16.10.22',
      time2: '13:55',
      state: 'working',
    },
    {
      condition: 'Номинальные обороты',
      data1: '09.10.22',
      time1: '10:12',
      data2: '15.10.22',
      time2: '10:11',
      state: 'not working',
    },
    {
      condition: 'Расход топлива норм',
      data1: '10.10.22',
      time1: '15:25',
      data2: '16.10.22',
      time2: '13:55',
      state: 'working',
    },
    {
      condition: 'Номинальные обороты',
      data1: '09.10.22',
      time1: '10:12',
      data2: '15.10.22',
      time2: '10:11',
      state: 'not working',
    },
    {
      condition: 'Расход топлива норм',
      data1: '10.10.22',
      time1: '15:25',
      data2: '16.10.22',
      time2: '13:55',
      state: 'working',
    },
  ]);

  const data = {
    test,
  };

  const datasize = test.value.length;
</script>

<style scoped></style>
