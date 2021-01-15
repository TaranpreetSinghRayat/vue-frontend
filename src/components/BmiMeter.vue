<template>
    <div class="BmiMeter">
        <v-img alt="meter"
          width="150" height="150" src="@/assets/img/bmi-meter.png"></v-img>
          <div class="marker" ref="marker" :style="{ top: `${this.top}px`, left: `${this.left}px`, transform: `rotateZ(${this.markerAngle}deg)` }"></div>
          <div class="meter-data">
              {{this.bmi}}
          </div>
    </div>
</template>
<script>
export default {
    props: ['bmi'],
  data() {
      return {
        top: 24,
        left: 19,
        angle: (35-19) * 14.0625 + 90,
        markerAngle: 0
      }
  },
  name: 'BmiMeter',
  methods: {
      setValues() {
        const markerheight = 30/2;
        const markerWidth = 25/2;
        this.angle = (35-this.bmi) * 14.0625 + 90;
        this.top = 75 - Math.sin(this.angle*Math.PI/180)*67 - markerheight;  
        this.left = 75 + Math.cos(this.angle*Math.PI/180)*67 - markerWidth;
      }
  },
  beforeMount() {
      this.setValues();
  },
  beforeUpdate() {
    this.setValues();
  }
}
</script>
<style >
    .meter-data {
        height: 95px;
        width: 95px;
        background: #515353;
        color: white;
        border-radius: 50%;
        position: absolute;
        top: 28px;
        left: 28px;
        display: flex;
        align-items: center;
        font-size: 2em;
        justify-content: center;
        font-weight: 1000;
    }

    .marker {
        width: 25px;
        height: 30px;
        border: 2px solid white;
        position: absolute;
    }
</style>