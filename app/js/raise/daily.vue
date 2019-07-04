<template lang="html">
    <Panel title="每日签到" :class="$style.panel">
        <section :class="$style.content">
            <img src="//m.secuunion.net/img/solutions.jpg" alt="">
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.panel {
    @include panel;
    > h4 {
        display: none;
    }
    .content {
        @include flex(row);
        // position: relative;
        // padding-bottom: 40px;
        margin-bottom: -20px;
        margin-top:100px;
        img {
            width: 100%;
            height: 100%;
        }
        // p {
        //     position: absolute;
        //     top: -112px;
        //     right: 20px;
        //     font-size: 28px;
        //     color: #999;
        //     height: 112px;
        //     line-height: 112px;
        // }
    }
}
</style>
