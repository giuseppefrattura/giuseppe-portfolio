<script setup>
const { data: posts } = await useAsyncData('posts', () =>
  queryContent('/blog').find()
)
</script>


<template>
    <h1 class="text-3xl my-8"> Blog posts</h1>

    Bla bla bla....

    <section class="grid md:grid-cols-3 mt-8 gap-10">
        <Post :posts ="posts"/>
    </section>

</template>