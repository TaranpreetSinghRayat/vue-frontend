<template>
    <div class="BmiMeter">
        <v-img alt="meter"
          width="150" src="@/assets/img/bmi-meter.png"></v-img>
          <div class="marker" :style="{ top: `${getValues(0)}px`, left: `${getValues(1)}px`, transform: `rotateZ(${getValues(2)}deg)` }"></div>
          <div class="meter-data">
              {{this.bmi}}
          </div>
    </div>
</template>
<script>
export default {
  data() {
      return {
          bmi: 20
      }
  },
  name: 'BmiMeter',
  methods: {
      getValues(type) {

          // TO-DO this function need update. one the bases of bim value return postion of marker 
          switch(type) {
            case 0: 
              return 29;
            case 1:
                return 19;
            case 2: 
                return 42;
          }
      }
  }
}
</script>
<style >
    .meter-data {
        height: 80px;
        width: 80px;
        background: #515353;
        color: white;
        border-radius: 50%;
        position: absolute;
        top: 41px;
        left: 42px;
        display: flex;
        align-items: center;
        justify-content: center;
        font-weight: 800;
    }

    .marker {
        width: 35px;
        height: 25px;
        border: 2px solid white;
        position: absolute;
    }
</style>