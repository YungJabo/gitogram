<template>
    <div class="topline">
        <topline>
            <template #headline>
                <div class="headline">
                    <span class="headline-text">Gitogram /</span>
                    <div class="icons-block">
                        <icon name="home" class="icons"></icon>
                        <icon name="photo" class="icons"></icon>
                        <icon name="exit" class="icons"></icon>
                    </div>
                </div>
            </template>

            <template #content>
                <ul class="stories">
                    <li class="stories-item" v-for="story in stories" :key="story.id">
                        <story-user-item :avatar="story.avatar" :username="story.username">
                        </story-user-item>
                    </li>
                </ul>
            </template>

            <template #comments-block>
                <topComment :avatar="stories[0].avatar" :username="stories[0].username"></topComment>
            </template>
        </topline>

    </div>
</template>

<script>
/* eslint-disable vue/multi-word-component-names */
/* eslint-disable */
import topline from '../../components/topline/topline'
import icon from '../../icons/icon'
import stories from './data.json'
import storyUserItem from '../../components/topline/storyUserItem/storyUserItem.vue'
import topComment from '@/components/topline/topComment/topComment.vue'

export default {
    name: 'feeds',
    components: {
        topline,
        icon,
        storyUserItem,
        topComment
    },
    data() {
        return {
            stories
        }
    }
}
</script>

<style lang="scss" scoped src="./feeds.scss"></style>
