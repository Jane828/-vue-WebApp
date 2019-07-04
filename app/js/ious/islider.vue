<template lang="html">
    <Panel title="轮播图" :class="$style.panel">
        <section :class="$style.content">
            <Slider :items="items"/>
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
                href: "home",
                src: "//m.secuunion.net/img/serva.jpg",
            }, {
                href: "home",
                src: "//m.secuunion.net/repository/image/bNpzAg9QQcaqJeZ4GvFiwA.jpg_1180xa.jpg",
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
        display: none;
    }
    margin-top: 100px;
    .content {
        img {
            width: 100%;
            height: 350px;
        }
    }
}
</style>
