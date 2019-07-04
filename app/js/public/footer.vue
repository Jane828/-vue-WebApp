<template lang="html">
    <Panel title="公司信息" :class="[$style.panel,cname]">
        <ul :class="$style.content">
            <li>
                <img src="//img12.360buyimg.com/jrpmobile/jfs/t2842/350/3035567089/14791/5f6ff93d/577cf395N31e76288.png?width=1125&height=252" alt="">
            </li>
            <li>
                <div>
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t2971/333/1297567079/898/f2d2e00d/577dc28dNe5138337.png?width=108&height=108" alt="">
                    <p>客户端</p>
                </div>
                <div>
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t2824/256/2966087355/831/188bfa25/577cf3dcN18aadbf2.png?width=108&height=108" alt="">
                    <p>触屏版</p>
                </div>
                <div>
                    <img src="//img12.360buyimg.com/jrpmobile/jfs/t2920/282/1283157010/1040/23f1430b/577cf3e5N53f740b8.png?width=108&height=108" alt="">
                    <p>电脑版</p>
                </div>
            </li>
            <li>
                <p>电话：0755-86375372</p>
                <p>邮箱：serryzeng@secuunion.net</p>
                <p>地址：深圳市南山区科研路9号比克科技大厦</p>
                <p>24楼2401-I单元</p>
                <p>Copyright&nbsp;©&nbsp;2018&nbsp;深圳市安盟信息科技有</p>
                <p>限公司.&nbsp;All Rights Reserved&nbsp;&nbsp;粤ICP备</p>
                <p>18155928号</p>
            </li>
        </ul>
    </Panel>
</template>

<script>
import Panel from "../core/panel.vue"
export default {
    components: {
        Panel,
    },
    props: {
        cname: {
            type: String,
            default: "",
        },
    },
}
</script>

<style lang="scss" module>
@import '../../css/element.scss';
.panel {
    @include panel;
    margin-bottom: 100px;
    & > h4 {
        display: none;
    }
    .content {
        @include flex;
        background-color: #f5f5f5;
        li {
            width: 100%;
            text-align: center;
            color: #999;
            font-size: 24px;
            > img {
                width: 100%;
                height: 100%;
            }
            &:nth-child(2) {
                @include flex(row);
                height: 186px;
                box-sizing: border-box;
                > div {
                    width: 33.3333%;
                    text-align: center;
                    box-sizing: border-box;
                    padding-top: 20px;
                    img {
                        width: 90px;
                        height: 90px;
                    }
                    p {
                        font-size: 26px;
                        text-align: center;
                        display: block;
                        color: #999;
                        margin-top: 12px;
                        white-space: nowrap;
                        text-overflow: ellipsis;
                        overflow: hidden;
                    }
                }
            }
            &:nth-child(n + 3) {
                // 表示从第三个元素开始生效
                background-color: #333333;
                padding: 40px 0 60px 0;
                > p {
                    text-align: left;
                    font-size: 20px;
                    padding: 15px 20px 0 20px;
                    &:nth-child(4),&:nth-child(6),&:nth-child(7){
                        padding: 0 20px 0 20px;
                    }
                }
            }
        }
    }
}
</style>
