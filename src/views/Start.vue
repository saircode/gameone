<template></template>

<script setup >
import { ref, reactive } from "vue";
import Phaser from '@/providers/phaser';
const phaser = Phaser.Phaser;

const config = reactive({
    type:phaser.AUTO,
    width: 800,
    height: 500,
    physics: {
        default: 'arcade',
        arcade: {
            gravity: {y:400},
            debug: false
        }
    }
});

const game = new phaser.Game(config);
</script>