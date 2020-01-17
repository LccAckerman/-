<template>
    <div>
        <div class="recommend-title">热销推荐</div> 
        <ul>
            <li class="item border-bottom" v-for="item of recommendList"
            :key="item.id">
                    <img class="item-img" src="item.imgUrl" />
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'HomeRecommend',
    data () {
        return {recommendList: [{
            id : "0001",
            imgUrl: "//img1.qunarzz.com/sight/p0/1605/58/5847560fd55ff6f590.water.jpg_256x160_13631f57.jpg",
            title: "凤凰古城",
            desc: "邂逅数个人，偶遇一座城"
        },{
            id : "0002",
            imgUrl: "//imgs.qunarzz.com/p/tts1/1912/ac/7b95ff10615dd902.jpg_256x144_2ac72bcf.jpg",
            title: "张家界",
            desc: "湘鄂渝黔革命根据地的发源地和中心区域"
        },{
            id : "0003",
            imgUrl: "//img1.qunarzz.com/sight/p0/1708/43/436d079f7f1df3dda3.water.jpg_256x160_87cfadb4.jpg",
            title: "天子山索道",
            desc: "天子山索道是单线循环式挂抱索器客运索道"
        }]}
    }
}
</script>

<style lang="stylus" scoped>
    @import "~styles/mixins.styl"
    .recommend-title{
        line-height :.8rem
        background :#eee
        text-indent :.2rem
        margin-top :.2rem
    }
    .item{
        display :flex
        height :1.9rem
        overflow :hidden
    }
    .item-img{
        width :1.7rem
        height: 1.7rem
        padding :.1rem
    }
    .item-info{
        flex : 1 //自动撑开宽度
        padding :.1rem
        min-width : 0
    }
    .item-title{
        line-height :.54rem
        font-size : .32rem
        ellipsis ()
    }
    .item-desc{
        line-height :.4rem
        color :#ccc
        ellipsis ()
    }
    .item-button{
        line-height :.44rem
        background :#ff9300
        padding :0 .2rem
        border-radius :.16rem
        margin-top :.14rem
        color :#fff
    }
</style>