<template>
<div id="content">
<grid-layout
    :layout.sync="layout"
    :col-num="1"
    :row-height="30"
    :is-draggable="true"
    :is-resizable="true"
    :is-mirrored="false"
    :vertical-compact="true"
    :margin="[10, 10]"
    :use-css-transforms="true">

    <grid-item v-for="item in layout"
                :x="item.x"
                :y="item.y"
                :w="item.w"
                :h="item.h"
                :i="item.i"
                :key="item.i">
        {{item.i}}
    </grid-item>
</grid-layout>
</div>
</template>

<script>

// @ is an alias to /src
import VueGridLayout from 'vue-grid-layout';

var testLayout = [
    {"x":0,"y":0,"w":2,"h":2,"i":"0"},
    {"x":0,"y":2,"w":2,"h":4,"i":"1"},
    {"x":0,"y":4,"w":2,"h":5,"i":"2"},
    {"x":0,"y":6,"w":2,"h":3,"i":"3"},

];

export default {
    name: 'ResumeTemp_Default',
    components: {
        GridLayout: VueGridLayout.GridLayout,
        GridItem: VueGridLayout.GridItem
    },
    data: function () {
    return {
       layout: testLayout,
     }  
    }
}
</script>