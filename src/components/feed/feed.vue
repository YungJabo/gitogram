<template>
    <div class="c-feed">
        <toggler @onToggle="toggle"></toggler>
        <div class="comments" v-if="shown">
            <ul class="comments-list">
                <li class="comments-item" v-for="n in 5" :key="n">
                    <comment text="some text" username="John Doe"></comment>
                </li>
            </ul>
        </div>
    </div>
</template>

<style lang="scss" scoped src="./feed.scss"></style>
<script>
/* eslint-disable */
import toggler from '../toggler/togglerComp.vue'
import comment from '../comment/comment.vue'

export default {
    name: 'feed',
    components: {
        comment,
        toggler
    },
    data () {
        return {
            shown: false
        };
    },
    methods: {
        toggle(isOpened){
            this.shown = isOpened;
        }
    }
}
</script>