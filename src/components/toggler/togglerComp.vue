<template>
    <button :class="['button', { active:isOpened }]" @click="toggle">
        <span class="text"> {{ isOpened ? "Hide" : "Show"}} issues
        </span>
        <span class="icon">
            <icon name="triangle"></icon>
        </span>
    </button>
</template>

<script>
/* eslint-disable vue/multi-word-component-names */
/* eslint-disable */
import icon from '../../icons/icon.vue'

export default {
    components: {
        icon,
    },
    data(){
        return{
            isOpened: false
        };
    },
    methods: {
        toggle (){
            this.isOpened = !this.isOpened;
            this.$emit('onToggle', this.isOpened);
        }
    }
}
</script>

<style lang="scss" scoped src="./toggler.scss"></style>