<template lang="html">
    <div :class="$style.header">
        <router-link :to="{name: 'ious'}">
            <img src="//m.secuunion.net/img/anmeng.png" alt="安盟信息科技" title="安盟信息科技">
        </router-link>
        <btn :class="$style.btnDownload">
            <router-link :to="{name: 'download'}">APP下载</router-link>
        </btn>
    </div>
</template>

<script>
import btn from "../core/btn.vue"
export default {
    components: {
        btn,
    },
}
</script>

<style lang="scss" module>
.header {
    background-color: rgba(9, 18, 49, 1);
    height: 100px;
    line-height: 100px;
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    z-index: 100;
    img {
        width: 256px;
        height: 61px;
        vertical-align: middle;
    }
    .btnDownload {
        float: right;
        font-size: 24px;
        border-width: 0;
        height: 46px;
        line-height: 46px;
        min-width: 100px;
        padding: 0 5px;
        border-radius: 4px;
        margin: 28px 24px 0 0;
        > a {
            color: #fff;
            text-decoration: none;
        }
    }
}
</style>
