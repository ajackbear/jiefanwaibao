<template>
  <div class="u-header">
    <div class="top-area">
        <div class="logo">
            <img src="@/assets/images/logo.png" />
        </div>
        <div class="search">
            <i class="icon iconfont icon-search-2-copy" />
            <input type="text" placeholder="Search products…" />
        </div>
        <div class="nav-menu" @click="navClick">
            <div class="menu-icon">
                <transition name="linetop">
                    <div class="menu-icon-item item-top" :class="menuShow == false ? 'menu-icon45' : ''"></div>
                </transition>                
                <transition name="line-center">
                    <div class="menu-icon-item item-center" :class="menuShow == false ? 'opacityLine' : ''"></div>
                </transition>
                <transition name="line-bottom">
                    <div class="menu-icon-item item-bottom" :class="menuShow == false ? 'menu-icon-45' : ''"></div>
                </transition>
            </div>
            Menu
        </div>
    </div>
    <div class="bottom-area">
        <transition name="mybox">
            <ul class="top-nav-area" ref="topNavArea" v-if="menuShow">
                <li class="nav-item">HOME</li>
                <li class="nav-item">STORE</li>
                <li class="nav-item">BEVERAGE</li>
                <li class="nav-item">BODY</li>
                <li class="nav-item">PET</li>
                <li class="nav-item">SPORTS</li>
                <li class="nav-item">COMMUNITY</li>
                <li class="nav-item">NEWS</li>
                <li class="nav-item">CONTACT</li>
            </ul>
        </transition>    
        <div class="shop-show-news">
            <span class="money">$<span>0.00</span></span>
            <span class="goods"><span>0</span>items</span>
            <i class="icon iconfont icon-lanzi" />
        </div>
    </div>
    <div class="bottom-nav">
        <div class="nav-item"><i class="icon iconfont icon-wode" /></div>
        <div class="nav-item"><i class="icon iconfont icon-search-2-copy" /></div>
        <div class="nav-item">
            <i class="icon iconfont icon-lanzi" />
            <div class="goods-tip">0</div>
        </div>
    </div>
  </div>
</template>

<script>
export default {
  name: 'UHeader',
  data()
  {
    return{
        menuShow: true
    }
  },
  methods:
  {
    /**
     * 点击菜单按钮
     */
    navClick()
    {
        this.menuShow = !this.menuShow;
    } 
  },
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style lang="less">
    @import "./header.less";
</style>
