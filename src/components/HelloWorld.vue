<template >
  <div class="flex flex-col w-[25.9vw] rounded-2xl h-[34.8vh] bg-[#30323D]">
    <div class="flex z-10 w-[25.9vw]    justify-between h-[3.8vh] gap-[0.83vw]  bg-[#30323D] shadow-md  shadow-[#272933]">
      <div class="flex  items-center w-[19vw] justify-between">
        <div class="flex ml-[1.04vw] items-center w-[6.1vw] text-[1.6vh] uppercase text-[#00FF94] ">Состояния</div>
        <div class="flex items-center w-[3.6vw] text-[0.92vh] text-[#D6EBFF]">Время начала</div>
      </div>
      <div class="flex items-center">
          <img src="src/img/vector.svg" class="h-[1.8vh]" />
      </div>
      <div class="flex items-center  w-[6.97vw] text-[0.92vh]  text-[#D6EBFF]">Время окончания</div>
    </div>
    <div class="flex items-center w-[25.9vw] h-[30.9vh] bg-[#30323D]">
    </div>
  </div>
</template>

<script setup>
defineProps({
  msg: {
    type: String,
    required: true
  }
})
</script>

<style scoped>
</style>
