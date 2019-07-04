<template lang="html">
    <Panel title="轮播图" :class="$style.panel">
        <section :class="$style.content">
            <Slider :items="items" :cname="$style.slider"/>
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
                src: "//m.secuunion.net/img/conax.jpg",
            }, {
                href: "home",
                src: "//www.secuunion.net/img/newsbar1.jpg",
            }],
        }
    },
}
</script>

<style lang="scss" module>
  @import "../../css/element.scss";
  .panel{
    @include panel;
    >h4{
      display: none;
    }
    .content{
      .slider{
        margin-top: 100px;
        img{
          width: 100%;
          height:274px;
        }
      }
    }
  }
</style>
