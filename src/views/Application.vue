<template>
  <div class="application">
    <BmiMeter class="meter-styles" :bmi="this.bmi"/>
    <web-cam class="webcam" autoplay ref="webcam"
        :selectFirstDevice="true"
        @started="onStarted"
        @stopped="onStopped"
        @error="onError"
        @cameras="onCameras"
        @camera-change="onCameraChange"
        />
    <v-btn class="app-btn" v-on:click="onCapture()">
        Capture
    </v-btn>
  </div>
</template>
<script>

import { WebCam } from "vue-web-cam";
import BmiMeter from "@/components/BmiMeter"

export default {
    data() {
        return {
            bmi: 19, // this value need to be updated.
            img: null,
            camera: null,
            deviceId: null,
            devices: []
        };
    },
    components: {
        WebCam,
        BmiMeter
    },
    methods: {
        onCapture() {
            this.img = this.$refs.webcam.capture();
            console.log(this.img);
        },
        onStarted(stream) {
            console.log("On Started Event", stream);
        },
        onStopped(stream) {
            console.log("On Stopped Event", stream);
        },
        onStop() {
            this.$refs.webcam.stop();
        },
        onStart() {
            this.$refs.webcam.start();
        },
        onError(error) {
            console.log("On Error Event", error);
        },
        onCameras(cameras) {
            this.devices = cameras;
            console.log("On Cameras Event", cameras);
        },
        onCameraChange(deviceId) {
            this.deviceId = deviceId;
            this.camera = deviceId;
            console.log("On Camera Change Event", deviceId);
        }
    }
}
</script>
<style>
.webcam {
    height: calc(100vh - 27px);
    background-color: black;
}

.meter-styles {
    position: absolute;
    right: 12px;
}
</style>
