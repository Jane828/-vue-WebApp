<template lang="html">
    <article class="">
        <Slider :items="items" :cname="$style.slider"/>
        <section :class="$style.list">
            <div :class="$style.itemClass" v-for="item in enters" :key="item.img">
                <router-link :to="{ name: item.href}">
                    <img :src="item.img" :alt="item.title">
                    <h4>{{ item.title }}</h4>
                </router-link>
            </div>
        </section>
    </article>
</template>

<script>
import Slider from "../core/slider.vue"
export default {
    components: {
        Slider,
    },
    data() {
        return {
            items: [{
                href: "raise",
                src: "//www.secuunion.net/repository/image/j8IVd2_wS9-LMTyhjsN8pA.jpg",
            }, {
                href: "raise",
                src: "//www.secuunion.net/repository/image/ipfob17sTSih304j6AJu9A.jpg",
            }, {
                href: "raise",
                src: "//www.secuunion.net/repository/image/UtKLAYSJTpqxd8rnUkZE-g.jpg",
            }],
            enters: [{
                href: "money",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t3991/64/2521945388/12110/93c0139/58d1e462Ncf294123.png?width=132&height=132",
                title: "优惠券",
            }, {
                href: "download",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t5590/252/875247023/17343/946aa72c/59224650N0f7ffc92.png?width=132&height=132",
                title: "领红包",
            }, {
                href: "money",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t4618/115/2179710654/11347/bf520df/58ec9d84Nfd169001.png?width=132&height=132",
                title: "领礼品",
            }, {
                href: "money",
                img: "//img12.360buyimg.com/jrpmobile/jfs/t5488/298/1036263348/12073/b4f4de97/590ac8e8Ne9def22e.png?width=135&height=135",
                title: "活动信息",
            }],
        }
    },
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.slider {
    margin-top: 100px;
    .swiper-button-prev,
    .swiper-button-next {
        display: none;
    }
    img {
        width: 100%;
        // 局部样式只影响当前业务组件，不影响抽象的复用组件
    }
}
.list {
    @include list(row);
    background: #fff;
    padding-top: 40px;
    padding-bottom: 20px;
    justify-content: space-around;
    a {
        text-decoration: none;
    }
    .itemClass {
        text-align: center;
        img {
            display: inline-block;
            width: 90px;
            height: 90px;
        }
        h4 {
            font-size: 26px;
            margin-top: 12px;
            color: #666;
        }
    }
}
</style>
