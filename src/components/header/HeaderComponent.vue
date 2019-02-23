<template>
    <nav class="nav">
        <div class="nav_brand"><span>Yi Syuan Jhan</span></div>
        <div class="nav_menu">
            <ul class="nav_menu_list">
                <li class="nav_menu_list_ele"><a href="#collection">作品集</a></li>
                <li class="nav_menu_list_ele"><a target="_blank" href="https://linkedin.com/in/逸宣-詹-529b21b9/"><i class="fab fa-linkedin"></i></a></li>
                <li class="nav_menu_list_ele"><a target="_blank" href="https://github.com/DakHarry"><i class="fab fa-github"></i></a></li>
                <li class="nav_menu_list_ele mobile--hidden"><span>Email: harry.jhan0301@gmail.com</span></li>
            </ul>
        </div>
    </nav>
</template>

<script>
export default {
    name: 'Header',
    data () {
        return {
        }
    },
    created () {
        window.addEventListener('scroll', this.checkScrollPos)
    },
    methods: {
        checkScrollPos () {
            let navEle = document.getElementsByClassName('nav')[0]
            if (0 < window.scrollY)
                navEle.classList.add("nav--skrolled")
            else
                navEle.classList.remove("nav--skrolled")
        }
    },
    mounted() {
        
    },
    destroyed() {
        window.removeEventListener('scroll', this.checkScrollPos)
    }

}
</script>

<style lang="sass" scoped>
    @import '../../assets/css/_variables.sass'
    .mobile--hidden
        @media screen and (max-width: 991px)
            display: none

    .nav
        display: flex
        flex-direction: row
        font-size: $font-size-base
        background-color: transparent
        color: $color-fff
        border-bottom: 1px solid $color-fff
        z-index: 2
        &.nav--skrolled
            background-color: $color-nav-bg
            color: $color-nav-title
            border-bottom: 1px $color-nav-title
            box-shadow: 1px 0 5px $color-nav-title
            position: fixed
            width: 100%
            & div.nav_menu ul.nav_menu_list li.nav_menu_list_ele
                & a, & span
                    color: $color-nav-title
                    &:hover
                        color: $color-main-orange
        & .nav_brand
            flex-basis: 30%
            padding: $nav-padding-tb 5% $nav-padding-tb 0
            margin-left: $margin-space
            font-size: 18px
            font-weight: $title-bolder
            letter-spacing: 0.5px
            transition: linear .2s
            @media screen and (min-width: 992px)
                flex-basis: 12%
        & .nav_menu
            display: flex
            flex-direction: row
            flex-grow: 1
            margin-right: $margin-space
            & .nav_menu_list
                display: flex
                justify-content: flex-end
                flex-direction: row
                font-size: $font-size-base
                font-weight: 600
                flex-basis: 100%
                & .nav_menu_list_ele > a
                    line-height: 50px
                    padding-left: 1.25em
                    padding-right: 1.25em
                    cursor: pointer
                    transition: linear .2s
                    outline: none
                    text-decoration: none
                    color: #fff
                    height: 100%
                    display: inline-block
                    width: 100%
                    text-align: center
                    &:hover, &:active
                        color: $color-main-orange
                    & > i
                        font-size: 1rem
                & .nav_menu_list_ele > span
                    transition: linear .2s
                    line-height: 50px
                    padding-left: 1.25em
                    padding-right: 1.25em
                    color: #fff
                    text-align: center

</style>
