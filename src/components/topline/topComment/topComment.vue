<template>
    <ul class="comment-blocks">
        <li class="comment-blok" v-for="n in 2" :key="n">
            <div class="human">
                <img :src="avatar" alt="" class="human__img">
                <span class="human__name">{{ username }}</span>
            </div>
            <div class="about">
                <h3 class="about__title">Vue.js</h3>
                <p class="about__text"></p>
                <div class="about__buttons">
                    <button class="star about__button"><img :src=star alt="" class="star__img"></button>
                    <span class="star-count about__button">156k</span>
                    <button class="fork about__button"><img :src=fork alt="" class="fork__img"></button>
                    <span class="fork-count about__button">4</span>
                </div>
            </div>
            <feed></feed>
        </li>
    </ul>
</template>

<style lang="scss" src="./topComment.scss" scoped></style>
<script>
/* eslint-disable vue/multi-word-component-names */
/* eslint-disable */
import feed from '../feed/feed.vue'
import star from '../../../../public/img/star.png'
import fork from '../../../../public/img/fork.png'
export default {
    name: 'topComment',
    components:{
        feed
    },
    props: {
        avatar: {
            type: String,
            required: true
        },
        username: {
            type: String,
            required: true
        }
    }

}
</script>
