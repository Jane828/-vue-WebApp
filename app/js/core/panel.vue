<template lang="html">
    <section :class="[panelClass,cname]">
        <h4>-{{ title }}-</h4>
        <slot/>
    </section>
</template>

<script>
export default {
    props: {
    // panel、slider、btn都为子组件,其它为对应的父组件,一子多父
        cname: {
            type: String,
            default: "",
        },
        title: {
            type: String,
            default: "",
        },
    },
    data() {
        return {
            panelClass: "panel",
        }
    },
}
</script>

<style lang="scss">
@import '../../css/element.scss';
.panel {
    @include panel;
    h4 {
        font-weight: bold;
    }
}
</style>
