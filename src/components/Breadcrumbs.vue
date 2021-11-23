<template>
<nav v-if="items && items.length"
    class="my-breadcrumbs"
>
    <ol>
        <li v-for="(item, itemIndex) in items" :key="itemIndex">
            <a v-if="itemIndex !== items.length - 1"
                :href="item.url"
                :title="item.name"
                class="bc-link"
            >
                {{ item.name }}
            </a>
            <span v-else class="bc-name">{{ item.name }}</span>
            <span v-if="items[itemIndex + 1]" class="bc-separator">/</span>
        </li>
    </ol>
</nav>
</template>

<script setup>
defineProps({
    items: {
        type: Array,
        required: true
    }
})
</script>

<style lang="scss" scoped>
.my-breadcrumbs {
    // background-color: #f7f7f7;
    // border-radius: 4px;
    ol, ul {
        list-style-type: none;
        display: flex;
        flex-direction: row;
        align-items: center;
        justify-content: flex-start;
        padding: 7px 15px;
        li {
            color: #222222;
            .bc-link {
                font-weight: 600;
                text-decoration: none;
                transition: all 0.5s ease;
                color: #222222;
                &:hover {
                    color: blue;
                    text-decoration: underline;
                }
            }
            // .bc-name {

            // }
            .bc-separator {
                color: hsla(0, 0%, 13%, 0.563);
                margin: 0.3rem;
            }
        }
    }
}
</style>
