<template>
    <div class="wrapper-content">
        <div class="content">
            <div class="locker"></div>
            <div class="content-body">
                <div class="content-left">
                    <h5 style="font-size: 0.9em; margin: 0; margin-bottom: 0.4em;">{{ title }}</h5>
                    <div class="cl-bottom">
                        <h4 class="btext" v-if="btext!=undefined">{{ btext }}</h4>
                        <p style="font-size: 0.8em; color:#666; margin: 0;">{{ text }}</p>
                    </div>
                </div>
                <div class="icon-slot">
                    <slot></slot>
                </div>
                <div class="rarr">
                    <i class="iconfont icon-forward"></i>
                </div>
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
defineProps(['title', 'text', 'btext'])
</script>

<style scoped>
.wrapper-content {
    margin: 0 1em;
}

.content {
    display: flex;
    align-items: center;
    background-color: white;
    border-radius: 3px;
    height: 4.8em;
}

.locker {
    width: 1em;
}

.content-body {
    display: flex;
    justify-content: space-between;
    align-items: center;
    background-color: white;
    height: 4.8em;
    width: 100%;
}

.cl-bottom {
    display: flex;
    align-items: center;
    width: 14em;
}

.cl-bottom p {
    overflow: hidden;
    text-overflow: ellipsis;
    white-space: nowrap;
    box-sizing: border-box;
}

.btext {
    font-size: 0.7em;
    color: #666;
    margin: 0;
    border-right: 1px solid #666;
    box-sizing: border-box;
    padding-right: 0.5em;
}

.rarr{
    width: 2em;
}
</style>