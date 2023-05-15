<template>
    <div class="c-topline">
        <div class="x-container">
            <div class="headline">
                <slot name="headline">

                </slot>
            </div>
            <div class="content" v-if="$slots.content">
                <slot name="content">

                </slot>
            </div>
        </div>
    </div>
</template>

<style lang="scss" src="./topline.scss" scoped></style>
<script>
/* eslint-disable vue/multi-word-component-names */
export default {
  name: 'topline'
  // определение компонента
}
</script>
