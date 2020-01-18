<template>
    <div>
        <div class="title">周末去哪儿</div> 
        <ul>
            <li class="item border-bottom" v-for="item of recommendList"
            :key="item.id">
            <div class="item-img-wrapper">
                    <img class="item-img" src="item.imgUrl" />
            </div>
                <div class="item-info">
                    <p class="item-title">{{item.title}}</p>
                    <p class="item-desc">{{item.desc}}</p>
                </div>
            </li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'HomeWeekend',
    data () {
        return {recommendList: [{
            id : "0001",
            imgUrl: "//imgs.qunarzz.com/vc/ad/7c/fe/037d1a400372ff57b0030d1d1c.jpg_92.jpg",
            title: "凤凰古城",
            desc: "邂逅数个人，偶遇一座城"
        },{
            id : "0002",
            imgUrl: "///imgs.qunarzz.com/vc/ad/7c/fe/037d1a400372ff57b0030d1d1c.jpg_92.jpg",
            title: "张家界",
            desc: "湘鄂渝黔革命根据地的发源地和中心区域"
        },{
            id : "0003",
            imgUrl: "//imgs.qunarzz.com/vc/ad/7c/fe/037d1a400372ff57b0030d1d1c.jpg_92.jpg",
            title: "天子山索道",
            desc: "天子山索道是单线循环式挂抱索器客运索道"
        }]}
    }
}
</script>

<style lang="stylus" scoped>
    @import "~styles/mixins.styl"
    .title{
        line-height :.8rem
        background :#eee
        text-indent :.2rem
    }
    .item-img{
        width :100%
    }
    .item-info{
        padding :.1rem
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
    .item-img-wrapper{
        height :0
        overflow : hidden 
        padding-bottom :33.9%
        }
</style>