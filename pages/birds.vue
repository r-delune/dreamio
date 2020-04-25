<template>
    <div class="container">
        <div class="vantabulous" ref="vantabulous" id="vantabulous">
        </div>
    </div>
</template>
<script>
import * as THREE from "three";
import NET from '~/static/vanta/dist/vanta.net.min';
import BIRDS from 'vanta/dist/vanta.birds.min'
import Logo from '~/components/Logo.vue'

export default {
  name: "THREETest",
    data: function() {
        return {
            vantaEffect: null,
            windowHeight: 0,
            txt: '',
            h: window.innerHeight, 
            w: window.innerWidth
        };
    },
    watch: {
        windowHeight(newHeight, oldHeight) {
            this.txt = `it changed to ${newHeight} from ${oldHeight}`;
        }
    },
    mounted() {
        this.vantaEffect = BIRDS({
            el: "#vantabulous",
            mouseControls: true,
            touchControls: true,
            minHeight: this.h,
            minWidth: this.w,
            lowlightColor: 0x3e14ff,
            baseColor: 0xf5e0e0,
            blurFactor: 0.20,
            speed: 3.90,
            zoom: 2.20,
            THREE: this.THREE
        })
    },
    onResize() {
        this.windowHeight = window.innerHeight
    },
    beforeDestroy() { 
        window.removeEventListener('resize', this.onResize); 
    }
};
</script>

<style>

</style>