<template lang="html">
    <Panel title="" :class="$style.panel">
        <section :class="$style.content">
            <router-link :to="{name: 'ious'}">
                <img src="//www.secuunion.net/img/jejuanner.jpg" alt="">
            </router-link>
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
    margin-bottom: 30px;
    > h4 {
        display: none;
    }
    .content {
        height: 102px;
        img {
            width: 100%;
            height: 135px;
        }
    }
}
</style>
