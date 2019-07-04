<template lang="html">
    <Panel title="产品信息" :class="$style.panel">
        <section :class="$style.content">
            <div :class="$style.item" v-for="item in items" :key="item.catory">
                <h4>{{ item.catory }}</h4>
                <section :class="$style.list">
                    <div :class="$style.product" v-for="product in item.list" :key="product.img">
                        <img :src="product.img" alt="">
                        <p :class="$style.title">{{ product.title }}</p>
                        <p :class="$style.price"><em>{{ product.price }}</em>起</p>
                        <article>
                            <div :class="$style.wrapper">
                                <div :class="$style.inner" :style="{width:product.progress+'%'}"/>
                            </div>
                            <p>{{ product.progress }}%</p>
                        </article>
                        <label v-if="product.tip">精选</label>
                    </div>
                </section>
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
    data() {
        return {
            items: [{
                catory: "SonicWall 防火墙",
                list: [{
                    img: "http://m.secuunion.net/repository/image/8Le4ynABSpCgOUR_0KGNAA.jpg_1180xa.jpg",
                    title: "NSA2650",
                    price: "18237.62",
                    progress: 172,
                    tip: true,
                }, {
                    img: "http://m.secuunion.net/repository/image/tQ2nLA_zSiy64vfGCSF8cA.jpg_1180xa.jpg",
                    title: "NSA4650",
                    price: "47485.04",
                    progress: 259,
                }],
            }, {
                catory: "网络安全入门级防火墙系列",
                list: [{
                    img: "http://m.secuunion.net/repository/image/8Err-rDHSsCKlRfcEpkR2g.jpg_1180xa.jpg",
                    title: "SOHO250",
                    price: "2600",
                    progress: 481,
                }, {
                    img: "http://m.secuunion.net/repository/image/BRKLzuMCRo6Vwl0k1lXqgw.jpg",
                    title: "TZ350",
                    price: "4500",
                    progress: 105,
                    tip: true,
                }],
            }, {
                catory: "网络安全装置(NSA2650~NSA9650)中端防火墙系列",
                list: [{
                    img: "http://m.secuunion.net/repository/image/LqryNUMsRQiqZqAKJWnFVg.jpg_1180xa.jpg",
                    title: "NSA5650",
                    price: "87946.22",
                    progress: 199,
                }, {
                    img: "http://m.secuunion.net/repository/image/3HkK8y3wS0WyVIaI3Yfp9g.jpg_1180xa.jpg",
                    title: "NSA9650",
                    price: "126550.43",
                    progress: 222,
                    tip: true,
                }],
            }, {
                catory: "XG Firewall 下一代防火墙",
                list: [{
                    img: "http://m.secuunion.net/repository/image/RMekzdnxSZKsiS5J7saoFQ.png_1180xa.png",
                    title: "XG85",
                    price: "28845",
                    progress: 199,
                    tip: true,
                }, {
                    img: "http://m.secuunion.net/repository/image/hwhLJuHcSu2kGsniQVob_Q.jpg_1180xa.jpg",
                    title: "XG650",
                    price: "57332",
                    progress: 222,
                }],
            }],
        }
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
            > h4 {
                font-size: 24px;
                color: #092f5b;
                height: 80px;
                line-height: 80px;
                margin-bottom:20px;
                text-align: center;
            }
            margin-bottom: 20px;
            .list {
                @include flex(row);
                .product {
                    width: 50%;
                    height: 396px;
                    box-sizing: border-box;
                    background: rgba(0, 0, 0, 0.02);
                    text-align: center;
                    position: relative;
                    img {
                        width: 180px;
                        height: 180px;
                        margin: 44px auto 20px;
                    }
                    .title {
                        font-family: PingFangSC-Medium;
                        font-size: 24px;
                        color: #444;
                    }
                    .price {
                        font-family: PingFangSC-Semibold;
                        font-size: 20px;
                        color: #999;
                        height: 48px;
                        line-height: 48px;
                        em {
                            font-size: 36px;
                            color: #ff3232;
                            margin-right: 4px;
                            &:before {
                                content: '￥';
                                font-size: 28px;
                            }
                        }
                    }
                    article {
                        @include flex(row);
                        align-items: center;
                        justify-content: space-around;
                        padding: 0 20px;
                        height: 30px;
                        line-height: 30px;
                        margin-top: 16px;
                        .wrapper {
                            width: 144px;
                            height: 10px;
                            background: #f6e6e6;
                            border-radius: 22px;
                            .inner {
                                width: 40%;
                                max-width: 100%;
                                height: 10px;
                                background-image: linear-gradient(
                                    270deg,
                                    #f55 1%,
                                    #ff9c31 100%
                                );
                                border-radius: 22px;
                            }
                        }
                        p {
                            font-size: 24px;
                            color: #999;
                        }
                    }
                    label {
                        position: absolute;
                        left: 0;
                        top: 0;
                        font-family: PingFangSC-Medium;
                        font-size: 20px;
                        color: #ff0000;
                        text-align: center;
                        padding: 4px 8px;
                        background-image: linear-gradient(
                            -35deg,
                            #c1c1c1 0,
                            #acacac 100%
                        );
                    }
                }
            }
        }
    }
}
</style>
