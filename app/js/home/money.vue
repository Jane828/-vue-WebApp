<template lang="html">
    <Panel title="合作伙伴" :class="$style.panel">
        <section :class="$style.list">
            <div :class="$style.item" v-for="item in items" :key="item.img">
                <router-link :to="{ name: item.href}">
                    <img :src="item.img" :alt="item.title">
                </router-link>
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
                href: "ious",
                img: "//m.secuunion.net/img/lnk1.png",
                title: "SONICWALL",
            }, {
                href: "ious",
                img: "//m.secuunion.net/img/lnk2.png",
                title: "SOPHOS",
            }, {
                href: "ious",
                img: "//m.secuunion.net/img/lnk3.png",
                title: "惠普",
            }, {
                href: "ious",
                img: "//m.secuunion.net/img/lnk4.png",
                title: "Informatica",
            }, {
                href: "ious",
                img: "//m.secuunion.net/img/lnk5.png",
                title: "思科",
            }, {
                href: "ious",
                img: "//m.secuunion.net/img/lnk6.png",
                title: "CiTRlX",
            }],
        }
    },
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.panel {
    @include panel;
    background: rgba(246, 246, 246, 1);
    .list {
        @include list(row);
        padding: 10px 0 40px 0;
        justify-content: space-around;
        a {
            text-decoration: none;
        }
        .item {
            text-align: center;
            img {
                display: inline-block;
                height: 49px;
                padding-bottom: 10px;
            }
        }
    }
}
</style>
