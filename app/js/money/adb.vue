<template lang="html">
    <Panel title="" :class="$style.panel">
        <section :class="$style.content">
            <router-link :to="{name: 'ious'}">
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t10876/23/2566835181/40527/d7d27c08/59f97d68Ne53fda5b.png?width=1080&height=240" alt="">
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
    > h4 {
        display: none;
    }
    .content {
        img {
            width: 100%;
            height: 142px;
            display: block;
        }
    }
}
</style>
