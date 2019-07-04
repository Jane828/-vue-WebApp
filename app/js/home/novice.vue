<template lang="html">
    <Panel title="关于安盟" :class="$style.panel">
        <section :class="$style.content">
            <div :class="$style.item">
                <router-link :to="{ name: 'raise'}">
                    <img src="//www.secuunion.net/img/shouabout.jpg" alt="">
                </router-link>
            </div>
            <div :class="$style.item">
                <h4>
                    安盟专注于企业的信息安全服务
                </h4>
                <p>
                    深圳市安盟信息科技有限公司于2011年创建。公司总部位于深圳，现已在上海，北京，长沙，厦门，西安等...
                </p>
                <btn :class="$style.btnDownload">
                    <router-link :to="{name: 'ious'}">
                        了解详情
                    </router-link>
                </btn>
            </div>
        </section>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
import btn from "../core/btn.vue"
export default {
    components: {
        Panel,
        btn,
    },
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.panel {
    @include panel;
    .content {
        @include list(row);
        .item {
            width: 50%;
            box-sizing: border-box;
            &:first-child {
                img {
                    width: 100%;
                    height: 100%;
                }
            }
            &:nth-child(2) {
                background-color: #f5f5f5;
                h4 {
                    padding: 40px 0 10px 15px;
                    color: #092f5b;
                    font-size: 20px;
                    font-weight: bold;
                }
                p {
                    padding: 20px 0 20px 15px;
                    font-size: 20px;
                    line-height: 24px;
                }
                .btnDownload {
                    background-color: #ff9900;
                    padding: 12px 24px;
                    margin-left: 15px;
                    border: none;
                    a {
                        color: #fff;
                        text-decoration: none;
                    }
                }
            }
        }
    }
}
</style>
