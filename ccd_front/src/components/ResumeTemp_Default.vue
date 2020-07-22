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
    {"x":0,"y":5,"w":2,"h":2,"i":"6"},
    {"x":0,"y":4,"w":2,"h":2,"i":"9"},
    {"x":0,"y":10,"w":2,"h":2,"i":"13"},
    {"x":0,"y":8,"w":2,"h":2,"i":"14"},
    {"x":0,"y":9,"w":2,"h":2,"i":"18"},
    {"x":0,"y":6,"w":2,"h":2,"i":"19"}
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