<script setup>
import Breadcrumbs from './components/Breadcrumbs.vue'

const myItems = [{
    name: 'IPOCS',
    url: 'https://ipocs.co'
}, {
    name: 'Articles',
    url: 'https://ipocs.co/articles'
}, {
    name: 'Web development tutorials',
    url: 'https://ipocs.co/articles?categorySlug=web-development'
}, {
    name: 'Simple breadcrumbs navigation VueJS 3 component',
    url: 'https://ipocs.co/article/foo-bar'
}]
</script>

<template>
    <Breadcrumbs :items="myItems" />
</template>
