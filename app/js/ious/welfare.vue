<template lang="html">
    <Panel title="客户成功案例" :class="$style.panel">
        <section :class="$style.content">
            <div :class="$style.item">
                <img src="//m.secuunion.net/repository/image/HlomsK_2S4G--OyEu4KQNQ.jpg" alt="">
                <div>
                    <h4>Dharma Kuthanur</h4>
                    <p>Transform Customer Experience with</p>
                </div>
                <em>查看更多 ></em>
            </div>
            <div :class="$style.item">
                <img src="//m.secuunion.net/repository/image/uVYAyFpdQQCnLOsOCDx8dQ.jpg" alt="">
                <div>
                    <h4>Vamshi Sriperumbudur</h4>
                    <p>What Can Businesses Learn from the</p>
                </div>
                <em>查看更多 ></em>
            </div>
            <div :class="$style.item">
                <img src="//m.secuunion.net/repository/image/uVYAyFpdQQCnLOsOCDx8dQ.jpg" alt="">
                <div>
                    <h4>Vamshi Sriperumbudur</h4>
                    <p>5-on-5: Foundational Big Data Management for Compelling Customer Experience</p>
                </div>
                <em>查看更多 ></em>
            </div>
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
        border-bottom: 1px solid #ddd;
    }
    .content {
        @include flex;
        .item {
            @include flex(row);
            align-items: center;
            height: 140px;
            &:after {
                content: ' ';
                box-sizing: border-box;
                height: 0;
                width: 100%;
                border-bottom: 1px solid #ddd;
                margin-left: 150px;
            }
            &:last-child:after {
                border-color: #fff;
            }
            > img {
                width: 88px;
                height: 88px;
                display: inline-block;
                margin: 0 32px;
            }
            > div {
                font-size: 32px;
                color: #333;
                line-height: 1.8;
                width: 304px;
                h4,
                p {
                    color: #999;
                    font-size: 24px;
                    line-height: 1.1;
                    white-space: nowrap;
                    text-overflow: ellipsis;
                    overflow: hidden;
                }
            }
            > em {
                color: #ff801a;
                font-size: 24px;
                margin-left: 40px;
            }
        }
    }
}
</style>
