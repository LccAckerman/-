<template>
    <div>
        <div class="title">周末去哪儿</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                <div class="item-img-wrapper">
                    <img class="item-img" :src=item.imgUrl />
                </div>
                <div class="item-info">
                    <p class="item-title">{{ item.title}}</p>
                    <p class="item-desc">{{ item.desc }}</p>
                </div>
            </li>
            <li></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'HomeWeekend',
    data () {
        return {
            recommendList: [{
            id: '001',
            imgUrl:'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
            title:"北京欢乐谷",
            desc:"亚洲唯一飞行式过山车等你来挑战"
        },{
            id: '002',
            imgUrl:'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
            title:"奥林匹克塔",
            desc:"今天的拚拚也要元气满满哦"
        },{
            id: '003',
            imgUrl:'http://img1.qunarzz.com/sight/source/1811/f3/86173f863bef61.jpg_r_640x214_52b003ac.jpg',
            title:"故宫",
            desc:"我要超级喜欢你！"
        }]
        }
    }
}
</script>

<style lang="stylus" scoped>
.title{
    margin-top :.2rem
    line-height :.8rem
    background-color :#eee
    text-indent :.2rem
}
// .item{
//     display :flex
//     height :1.9rem
//     overflow :hidden
// }
.item-img{
    width : 100%
}
.item-info{
    padding :.1rem
}
.item-title{
    line-height :.54rem
    font-size :.32rem
    text-overflow: ellipsis	
}
.item-desc{
    line-height :.4rem
    color :#ccc
    text-overflow: ellipsis
}
.item-img-wrapper{
    height :0
    overflow :hidden
    padding-bottom : 33.9%
}
</style>