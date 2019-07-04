<template lang="html">
    <Panel title="下载APP" :class="$style.panel">
        <section :class="$style.content">
            <img src="//m.secuunion.net/img/anmeng.png" alt="安盟信息科技" title="安盟信息科技">
            <p>立即下载</p>
        <!-- <span>copyright</span> -->
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
// html,
// body {
//     background: #fff;
// }
.panel {
    @include panel;
    margin: 0 !important;
    > h4 {
        display: none;
    }
    .content {
        @include flex;
        justify-content: center;
        align-items: center;
        height: 1136px;
        width: 100%;
        background-color: #091231;
        > img {
            // background: url('//m.secuunion.net/img/anmeng.png') center center no-repeat;
            width: 85%;
            height: 12%;
            display: block;
            // background-size: 100% auto;
            margin-top: -400px;
        }
        > p {
            @include btn(
                $size: 32px,
                $color: #fff,
                $bgcolor: #104a7e,
                $padding: 5px,
                $radius: 10px
            );
            height: 100px;
            line-height: 100px;
            width: 471px;
            background-image: linear-gradient(
                270deg,
                #3084b8 0,
                #104a7e 75%
            );
            box-shadow: 0 12px 32px 0 rgb(16, 128, 245);
            position: fixed;
            bottom: 200px;
        }
        // span {
        //     position: fixed;
        //     bottom: 16px;
        //     font-size: 24px;
        //     color: #eee;
        // }
    }
}
</style>
