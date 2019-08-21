<template>
    <div class="icons">
        <swiper>
            <swiper-slide>
                <div class="icon" v-for="item of iconList" :key="item.id">
                    <div class="icon-img">
                        <img class="icon-img-content" :src="item.imgUrl"/>
                        <p class="icon-desc">{{ item.desc }}</p>
                    </div>
                </div>
            </swiper-slide>
        </swiper>
    </div>
</template>

<script>
export default {
    name: "HomeIcons",
    data () {
        return {
            iconList: [{
                id: "0001",
                imgUrl: "//s.qunarzz.com/homenode/images/touchheader/hotel.png",
                desc: "酒店"
            },{
                id: "0002",
                imgUrl: "//s.qunarzz.com/homenode/images/touchheader/flight.png",
                desc: "机票"
            },{
                id: "0003",
                imgUrl: "//s.qunarzz.com/homenode/images/touchheader/package.png",
                desc: "度假"
            },{
                id: "0004",
                imgUrl: "//s.qunarzz.com/homenode/images/touchheader/train.png",
                desc: "火车票"
            },{
                id: "0005",
                imgUrl: "//s.qunarzz.com/homenode/images/touchheader/piao.png",
                desc: "景点门票"
            },{
                id: "0006",
                imgUrl: "//s.qunarzz.com/homenode/images/touchheader/group.png",
                desc: "特惠酒店"
            },{
                id: "0007",
                imgUrl: "//s.qunarzz.com/homenode/images/touchheader/bargainflight.png",
                desc: "低价机票"
            },{
                id: "0008",
                imgUrl: "//s.qunarzz.com/homenode/images/touchheader/inn.png",
                desc: "机票"
            },{
                id: "0009",
                imgUrl: "//s.qunarzz.com/homenode/images/touchheader/haiwai.png",
                desc: "海外酒店"
            }]
        }
    },
    computed: {
        pages (){
            const pages = []
            this.iconList.forEach((item, index) => {
                const page = Math.floor(index/8)
                if (!pages[page]){
                    pages[page] = []
                }
                pages[page].push(item) 
            })
            return pages
        }
    }
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl';
.icons >>> .swiper-container{
    height : 0
    padding-bottom :50% //这样的宽高比是二
    margin-top :.1rem
    }
.icon{
    position :relative
    overflow :hidden
    width :25%
    height :0
    float :left
    padding-bottom :25%
}
.icon-img{
    position :absolute
    top :0
    left :0
    right :0
    bottom :.44rem
    box-sizing :border-box
    padding :.1rem
}
.icon-img-content{
    display :block
    height :100%
    margin :0 auto
    height :100%
}
.icon-desc{
    position :absolute
    left :0
    right :0
    line-height :.44rem
    height :.44rem
    color :$darkTextColor
    text-align :center
}
</style>