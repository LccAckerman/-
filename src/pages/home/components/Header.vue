<template>
    <div class="header">
        <div class="header-left">
            <div class="iconfont back-icon">&#xe624;</div>
        </div>
        <div class="header-input">
            <span class="iconfont">&#xe632;</span>
            输入城市/景点/游玩主题
            </div>
        <div class="header-right">
            城市
            <span class="iconfont arrow-icon">&#xe64a;</span>
            </div>
    </div>
</template>

<script>
export default {
  name: 'HomeHeader'
}
</script>

<style lang="stylus" scoped>
@import '~styles/variables.styl'
1rem = html font-size = 50px
.header{
    line-height : .86rem
    display : flex
    background-color : $bgColor
    color : #fff
}
.header-left{
    width : .64rem
    float : left 
}
.header-input{
    flex : 1
    padding-left :.2rem
    line-height : .64rem
    margin-top : .12rem
    margin-bottom  : .12rem
    margin-left  : .2rem
    background-color : #ffffff
    border-radius : .1rem
    color : #cccccc
}
.header-right{
    width : 1.24rem
    float : right
    text-align : center 
}
.back-icon{
    text-align :center
    font-size :.4rem
}
.arrow-icon{
    font-size :.2rem
    margin-left :-.04rem
}
</style>
