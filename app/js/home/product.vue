<template lang="html">
    <Panel title="公司动态" :class="$style.panel">
        <section :class="$style.content">
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
                src: "//www.secuunion.net/repository/image/UtXLCCiETh67DjvTGHa1NQ.jpg",
                title: "构建高速无线网络安全解决方案",
                content: "通过 SonicWall 网络安全服务和我们防火墙硬件的附加组件，保护您的组织免受高级安全威胁，获得更大的安全控制，提高...",
            }, {
                href: "raise",
                src: "//www.secuunion.net/repository/image/0a6QxCKFRNqqE9REsMIpKg.jpg",
                title: "在高性能安全平台上实现高级威胁预防",
                content: "通过 SonicWall 网络安全服务和我们防火墙硬件的附加组件，保护您的组织免受高级安全威胁，获得更大的安全控制，提高...",
            }, {
                href: "raise",
                src: "//www.secuunion.net/repository/image/-_jrfQK0S5CpAoLtQyceWA.jpg",
                title: "构建高速无线网络安全解决方案",
                content: "通过 SonicWall 网络安全服务和我们防火墙硬件的附加组件，保护您的组织免受高级安全威胁，获得更大的安全控制，提高...",
            }],
            options: {
                slidesPerView: 1,
                spaceBetween: 1,
                loop: true,
                arrowBtn: true,
                Info: true,
                navigation: {
                    nextEl: ".swiper-button-next",
                    prevEl: ".swiper-button-prev",
                },
            },
        }
    },
}
</script>

<style lang="scss">
.product-slider {
    .swiper-container {
        box-sizing: border-box;
        padding: 0;
        .swiper-slide {
            a {
                display: inline-block;
                img {
                    width: 100%;
                    height: 40%;
                    display: block;
                }
            }
            div {
                padding: 0 15px;
            }
            div > h4 {
                font-size: 20px;
                font-weight: bold;
                color: #092f5b;
                padding: 15px 0 10px 0;
            }
            div > p {
                font-size: 20px;
                flex-direction: row;
                line-height: 24px;
            }
        }
    }
}
</style>

<style lang="scss" module>
@import '../../css/element.scss';
.panel {
    @include panel;
    .content {
        padding-bottom: 40px;
    }
}
</style>
