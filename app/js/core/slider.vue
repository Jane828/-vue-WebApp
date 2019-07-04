<template lang="html">
    <section :class="cname">
        <swiper :options="options" :not-next-tick="options.notNextTick">
            <swiper-slide v-for="item in items" :key="item.href">
                <router-link :to="{ name: item.href}">
                    <img :src="item.src" alt="">
                </router-link>
                <div v-if="options.Info">
                    <h4>{{ item.title }}</h4>
                    <p>{{ item.content }}</p>
                </div>
            </swiper-slide>
            <div class="swiper-pagination" v-if="options.pagination" slot="pagination"/>
            <div class="swiper-button-prev" v-if="options.arrowBtn" slot="button-prev"/>
            <div class="swiper-button-next" v-if="options.arrowBtn" slot="button-next"/>
        </swiper>
    </section>
</template>

<script>
import { swiper, swiperSlide } from "vue-awesome-swiper"
export default {
    components: {
        swiper,
        swiperSlide,
    },
    props: {
        cname: {
            type: String,
            default: "",
        },
        options: {
            type: Object,
            default() {
                return {
                    autoplay: true,
                    // 自动切换
                    loop: true,
                    // 循环模式
                    pagination: {
                        // pagination:分页器设置
                        el: ".swiper-pagination",
                        clickable: true,
                    },
                    notNextTick: false,
                    arrowBtn: false,
                    Info: false,
                    // 是一个组件自有属性，如果notNextTick设置为true，组件则不会通过NextTick来实例化swiper，也就意味着你可以在第一时间获取到swiper对象，假如你需要刚加载遍使用获取swiper对象来做什么事，那么这个属性一定要是true
                }
            },
        },
        items: {
            type: Array,
            default() {
                return []
            },
        },
    },
}
</script>

<style lang="css">
@import '~swiper/dist/css/swiper.css';
</style>
