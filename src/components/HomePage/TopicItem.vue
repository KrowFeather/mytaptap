<template>
    <div class="wrapper">
        <header>
            <div class="header-left">
                <div class="topic-title">
                    <h4>#{{ title }}</h4>
                    <div class="info">
                        <div class="emoji">
                            <img :src="emoji" alt="" style="width: 1.1em;">
                        </div>{{ info }}
                    </div>
                </div>
                <div class="topic-subtitle">{{ subtitle }}</div>
            </div>
            <div class="header-right">
                <el-button class="btn" size="small">去发布</el-button>
            </div>
        </header>
        <div class="bottom">
            <div class="bottom-pic" v-for="(item, i) in pics" :key="i">
                <img :src="item" alt="" style="height: 6.5em; width: 95%; object-fit: cover; border-radius: 3px;">
            </div>
        </div>
    </div>
</template>

<script lang="ts" setup>
defineProps(['title', 'info', 'subtitle', 'pics', 'emoji'])

</script>

<style scoped>
.wrapper {
    width: 100%;
    box-sizing: border-box;
    padding: 0 1em;
    background-color: white;
}

header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    box-sizing: border-box;
    padding-right: 0.3em;
}

.header-left {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
}

.header-left .topic-title {
    display: flex;
    justify-content: flex-start;
    align-items: center;
    width: 100%;
    margin: 0.5em 0;
}

.header-left .topic-title h4 {
    margin: 0;
}

.header-left .topic-title .info {
    border: 1px solid #ddd;
    border-radius: 3px;
    color: #666;
    margin-left: 0.5em;
    font-size: 0.7em;
    padding: 0 0.3em;
}

.header-left .topic-subtitle {
    font-size: 0.8em;
    color: #666;
    width: 100%;
}

.bottom {
    display: flex;
    margin-top: 0.5em;
}

.bottom-pic {
    width: 33.3%;
    height: 100%;
}

.emoji{
    display:flex;
    justify-content: center;
    align-items: center;
}
.info{
    display: flex;
}

.btn{
    background-color: #01c2c1;
    color: white;
}
</style>