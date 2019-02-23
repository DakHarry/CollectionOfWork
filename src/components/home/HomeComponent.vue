<template>
    <section class="content">
        <div class="content_bn">
            <div class="content_intro">
                Hi, My name is 詹逸宣(Yi-Syuan Jhan). I worked as an IT team leader and .NET full-stack developer with three-years experience in the organic farming e-commerce startup. 
                I am a communicative and outgoing team player. <br/><br/>
                Besides, I am an active learner who loves to challenge myself and solve the problems.
            </div>
        </div>
        <div class="content_collections">
            <h1 id="collection" class="content_collection_title">作品集</h1>
            <ul class="content_collection_list">
                <li class="content_collection_list_ele" :key="'public-'+c.id" v-for="c in collections">
                    <a class="list_ele_frame" target="_blank" :href="c.link">
                        <div class="list_ele_img">
                        <img :src="c.image" :alt="c.title">
                        </div>
                        <div class="list_ele_desc">
                            <div class="ele_desc_title">{{c.title}}</div>
                            <div class="ele_desc_text" v-html="c.description"></div>
                            <div class="ele_desc_tags">
                                <span :key="'tag-'+t" v-for="t in c.tags">{{t}}</span>
                            </div>
                        </div>
                    </a>
                </li>
            </ul>
        </div>
    </section>
</template>

<script>
export default {
    name: 'Home',
    data () {
        return {
            msg: '首頁資訊',
            collections: [{
                id: 1,
                title: 'Greenbox.tw',
                description: 'A pioneer in organic farming E-commerce startup in Taiwan contributes to solving the problems of agriculture. Builds the channel between the organic farmers and the customers to achieve a win-win situation. The company expands the storehouse and the store to provide more flexible services to customers in 2 years.',
                image: 'https://greenbox.tw/Images/NewIndex/New_logo.png',
                link: 'https://greenbox.tw/',
                tags: ['.NET MVC','C#', 'jQuery', 'Scss', 'Azure', 'LINQ', 'MS SQL', 'Gulp', 'Git']
            },{
                id: 2,
                title: 'Go through Progressive Web Apps (PWAs) within 30 days',
                description: "A simple blogger demo implements the concepts and the features of PWAs.<br/> It's a 30 days challenge held by Taiwan ITHome community in 2018. I took PWAs as my subject to share the concepts of PWAs and wrote the technology articles continuously for 30 days.",
                image: 'https://firebasestorage.googleapis.com/v0/b/collectionofmywork-c3af4.appspot.com/o/pwa-icon.png?alt=media&token=1cad869b-373c-4fe5-9d7a-9b3a28af0796',
                link: 'https://github.com/DakHarry/30day-pwas-practice',
                tags: ['PWAs','Firebase', 'Javascript']
            },{
                id: 3,
                title: 'F2E Challenge Week1: TodoList',
                description: "It's a coding challenge held by Taiwan front-end community in 2018.<br/> The community provided a design layout and the members required to build in one week with any language. I implemented with Vue2.js and host on Heroku.",
                image: 'https://firebasestorage.googleapis.com/v0/b/collectionofmywork-c3af4.appspot.com/o/f2e_w1.PNG?alt=media&token=b2392a39-bb93-448e-a697-615d8540a445',
                link: 'https://dakharry.github.io/F2E_Week1_TodoList/dist/index',
                tags: ['Vue2','json-server', 'Flexbox', 'Scss', 'heroku']
            },{
                id: 4,
                title: 'F2E Challenge Week2: Filter Page',
                description: "It's a coding challenge held by Taiwan front-end community in 2018.<br/>The project practice to connect the open source data from the government to implement the search feature.",
                image: 'https://firebasestorage.googleapis.com/v0/b/collectionofmywork-c3af4.appspot.com/o/f2e_w2.PNG?alt=media&token=90b82cdd-1470-4553-8886-8c9e1d03e100',
                link: 'https://f2e-filter.firebaseapp.com/',
                tags: ['Angular6','Firebase', 'Bootstrap4']
            },{
                id: 5,
                title: 'F2E Challenge Week3: Admin Page',
                description: "It's a coding challenge held by Taiwan front-end community in 2018.<br/> To build a simple admin control panel.",
                image: 'https://firebasestorage.googleapis.com/v0/b/collectionofmywork-c3af4.appspot.com/o/f2e_w3.PNG?alt=media&token=516a5960-a598-45e2-a26b-effd688ca1bc',
                link: 'https://f2e-week3.firebaseapp.com/',
                tags: ['Vue2','Firebase', 'Bootstrap4']
            },{
                id: 6,
                title: 'Git Blog',
                description: "A simple blog for recording the concepts of Git built with HTML5. Besides, Used as training material to train team member in Soohoobook Inc.",
                image: 'https://firebasestorage.googleapis.com/v0/b/collectionofmywork-c3af4.appspot.com/o/git-demo.PNG?alt=media&token=524b9372-afd3-4681-93ad-7596d68fe69c',
                link: 'https://dakharry.github.io/gitDemo1/',
                tags: ['Git']
            },{
                id: 7,
                title: 'Understand the current website by ASP.NET MVC 5',
                description: "•	Learns the whole concepts of ASP.NET MVC 5 and reorganizes with my thoughts to share through articles.",
                image: 'https://ithelp.ithome.com.tw/storage/image/logo.svg',
                link: 'https://ithelp.ithome.com.tw/users/20103808/ironman/1190',
                tags: ['.NET MVC','blog']
            }]
        }
    }
}
</script>

<style lang="sass" scoped>
    @import '../../assets/css/_variables.sass'
    .content
        display: flex
        flex-direction: column
        margin-bottom: 40px
    .content_bn
        z-index: -1
        width: 100%
        height: 450px
        top: -50px
        position: relative
        background-size: cover
        background-image: url("../../assets/images/bn.jpg")
        background-repeat: no-repeat
        background-position: center
        @media screen and (min-width: 768px)
            height: 650px
        & .content_intro
            position: absolute
            display: inline-flex
            margin: 0 5%
            background-color: #f0f2f76b
            top: 50%
            transform: translate(0, -50%)
            padding: 2% 20px
            border-radius: 10px
            font-size: 1.25rem
            line-height: 28px
            border: 1px solid #cec9c9
            box-shadow: 1px 1px 2px #eaeaea
            text-align: justify
            @media screen and (min-width: 768px)
                margin: 0
                width: 500px
                right: 15%
    .content_collections
        margin: 0 5%
        @media screen and (min-width: 992px)
            margin: 0 15%
        & .content_collection_title
            font-size: 1.25rem
            font-weight: 900
            line-height: 28px
            color: $color-000
            border-bottom: 2px solid #f7f7f7
            margin-bottom: 15px
            padding-bottom: 5px
        & .content_collection_list
            display: flex
            flex-direction: column
            & li.content_collection_list_ele
                margin-bottom: 20px
                border-radius: 5px
                display: flex
                border: 1px solid #ececec
                position: relative
                transition: all .2s
                box-shadow: 1px 1px 4px #efefef
                &:hover, &:active, &:focus
                    border: 1px solid #F19149
                    color: $color-000
                    top: -5px
                & a.list_ele_frame
                    width: 100%
                    display: flex
                    flex-wrap: nowrap
                    flex-direction: column
                    padding: 20px 10px
                    outline: none
                    text-decoration: none
                    @media screen and (min-width: 992px)
                        flex-direction: row
                    & .list_ele_img
                        margin-bottom: 20px
                        text-align: center
                        align-self: center
                        @media screen and (min-width: 992px)
                            flex-basis: 250px
                            margin-bottom: 0px
                        & > img
                            max-width: 250px
                    & .list_ele_desc
                        flex-basis: 70%
                        padding-left: 2rem
                        & .ele_desc_title
                            margin-bottom: 10px
                            font-size: 1.25rem
                            color: $color-000
                        & .ele_desc_text
                            margin-bottom: 10px
                            font-size: 1rem
                            color: $color-000
                            line-height: 24px
                            text-align: justify
                        & .ele_desc_tags
                            margin-bottom: 10px
                            & span
                                font-size: 1rem
                                padding: 2px 5px
                                border-radius: 11px
                                margin-right: 10px
                                background-color: #ff6e3a
                                border: 1px solid #ff6e3a
                                color: #fff
                                min-width: 50px
                                display: inline-block
                                text-align: center
                                margin-bottom: 3px

</style>
