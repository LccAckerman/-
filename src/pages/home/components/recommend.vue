<template>
    <div>
        <div class="title">热销推荐</div>
        <ul>
            <li class="item border-bottom" v-for="item of recommendList" :key="item.id">
                    <img class="item-img" :src=item.imgUrl />
                <div class="item-info">
                    <p class="item-title">{{ item.title}}</p>
                    <p class="item-desc">{{ item.desc }}</p>
                    <button class="item-button">查看详情</button>
                </div>
            </li>
            <li></li>
        </ul>
    </div>
</template>

<script>
export default {
    name: 'HomeRecommend',
    data () {
        return {
            recommendList: [{
            id: '001',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1508/89/895a1b7add84f23faca053ce9e3153db.water.jpg_200x200_99ae30ee.jpg',
            title:"北京欢乐谷",
            desc:"亚洲唯一飞行式过山车等你来挑战"
        },{
            id: '002',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1804/1a/1a48cc20b0d6ed44a3.img.jpg_200x200_32e22bed.jpg',
            title:"奥林匹克塔",
            desc:"今天的拚拚也要元气满满哦"
        },{
            id: '003',
            imgUrl:'http://img1.qunarzz.com/sight/p0/1409/19/adca619faaab0898245dc4ec482b5722.jpg_200x200_1bc99086.jpg',
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
.item{
    display :flex
    height :1.9rem
    overflow :hidden
}
.item-img{
    width :1.7rem
    height :1.7rem
    padding :.1rem
}
.item-info{
    flex :1
    min-width :0
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
.item-button{
    line-height :.44rem
    background-color #ff9300
    padding:0 .1rem
    border-radius :.06rem
    margin-top :.16rem
}
</style>