<template lang="html">
    <Panel title="更多方案" :class="$style.panel">
        <section :class="$style.content">
            <div :class="$style.item" v-for="item in items" :key="item.img">
                <router-link :to="{ name: 'raise'}">
                    <img :src="item.img" alt="">
                </router-link>
                <h4>{{ item.title }}</h4>
                <p>{{ item.text }}</p>
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
                img: "//m.secuunion.net/repository/image/jqs3xzdfSTi1iyZ_4AxqPA.png",
                title: "创建智能数据湖",
                text: "Informatica Enterprise Data Lake 提供的可信、相关和可行性信息，可为您的云端或本地数据湖赋能。有了它，您的用户能以一种独特的协作方式来快速查找、准备和管控大数据资产，从而快速制定决策。",
            }, {
                img: "//m.secuunion.net/repository/image/VtMhGHxmTn-WpIcsTJXEXg.png",
                title: "通过自助服务更快地实现价值",
                text: "Informatica Enterprise Data Lake 的数据准备功能借力人工智能和机器学习技术，为自助分析服务提档升级。从此无需手动整理数据，您的分析人员可以共享和重复使用流程，从而更快地获得洞察力。",
            }, {
                img: "//m.secuunion.net/repository/image/uZ3NWplGSPav0ek4NAcJGA.png",
                title: "迁移到云数据仓库 ",
                text: "使用 Informatica Enterprise Data Catalog 和 Big Data Management，可以对要迁移到全新云数据仓库的数据进行编目和识别；然后，在将数据移动到 Amazon Redshift、Azure SQL 数据仓库或 Google Big Query 之前，摄取、集成和扩充数据。",
            }, {
                img: "//m.secuunion.net/repository/image/f1ZVOzlbTXyPyE2rX9_L3Q.png",
                title: "迁移到云数据仓库",
                text: "当您分析流数据时，得到的见解会更明智。通过人工智能驱动的 Informatica Big Data Streaming，您可以基于流数据进行感知、推理并采取行动。并且，在您需要时，Edge Data Streaming 可以实时或批量地提供数据。",
            }],
        }
    },
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.panel {
    @include panel;
    .content {
        @include flex(row);
        justify-content: space-around;
        .item {
            width: 220px;
            height: 100%;
            text-align: center;
            margin-bottom: 10px;
            img {
                width: 220px;
                height: 100%;
            }
            h4 {
                font-size: 22px;
                color: #092f5b;
                margin-bottom: 12px;
            }
            p {
                font-size: 16px;
                color: #666;
                text-align: left;
            }
        }
    }
}
</style>
