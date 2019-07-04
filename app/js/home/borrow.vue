<template lang="html">
    <Panel title="推荐产品" :class="$style.panel">
        <section :class="$style.content">
            <div class="arrow">更多尖货 ></div>
            <Slider :options="options" :items="items" cname="product-slider"/>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import Slider from "../core/slider.vue"
export default {
    components: {
        Panel,
        Slider,
    },
    data() {
        return {
            items: [{
                href: "raise",
                src: "//www.secuunion.net/repository/image/hwhLJuHcSu2kGsniQVob_Q.jpg",
            }, {
                href: "raise",
                src: "//www.secuunion.net/repository/image/RMekzdnxSZKsiS5J7saoFQ.png",
            }, {
                href: "raise",
                src: "//2f.zol-img.com.cn/product/188_120x90/73/ceRKTlcEE2A.jpg",
            }, {
                href: "raise",
                src: "//www.secuunion.net/repository/image/LqryNUMsRQiqZqAKJWnFVg.jpg",
            }, {
                href: "raise",
                src: "//www.secuunion.net/repository/image/8Err-rDHSsCKlRfcEpkR2g.jpg",
            }, {
                href: "raise",
                src: "//2e.zol-img.com.cn/product/181_120x90/766/ceii4xIVanPn.jpg",
            }, {
                href: "raise",
                src: "//2c.zol-img.com.cn/product/141_120x90/466/ce0D6PwVTgWHM.jpg",
            }],
            options: {
                slidesPerView: 2.3,
                // 设置slider容器能够同时显示的slides数量,为2.3张
                spaceBetween: 30,
                // 在slide之间设置距离（单位px）
                freeMode: true,
                // free模式，slide会根据惯性滑动且不会贴合

                // 轮播指示圆点
                // pagination: {
                //     el: ".swiper-pagination",
                //     clickable: true,
                // },
            },
        }
    },
}
</script>

<style lang="scss">
.product-slider {
    // 自定义的组件与第三方的样式组合使用
    // 这里不启用css module,不然第三方内置的类.swiper-container的样式会无效
    .swiper-container {
        box-sizing: border-box;
        padding: 0 24px;
        .swiper-slide {
            a {
                display: inline-block;
                width: 100%;
                img {
                    width: 100%;
                    height: 100%;
                    display: block;
                    border: 1px solid #fafafa;
                }
            }
        }
    }
}
</style>

<style lang="scss" module>
@import '../../css/element.scss';
.panel {
    @include panel;
    // 继承子组件panel并进行样式覆盖
    .content {
        padding-bottom: 40px;
        position: relative;
        & > div {
            position: absolute;
            font-size: 22px;
            color: #999;
            right: 20px;
            top: -66px;
        }
    }
}
</style>
