<script setup>
const { data: posts } = await useAsyncData('latest-posts', () =>
  queryContent('/blog')
  .sort({data:1})
  .limit(3)
  .find()
)
</script>

<template>
    <section>
        <h1 class="text-5xl font-bold mt-20">Ciao, sono Giuseppe Frattura</h1>
        <p class="text-base p-2 italic">DevOps Engineer in MDOTM</p>
    </section>
    <section class="flex flex-col " >
        <h2 class="text-3xl font-bold mt-8">La mia storia</h2>
        <p>PEPepepepeksfjhbdksjnfkjsnflksdl</p>
    </section>
    <section>
        <h2>Latest post</h2>
        <div class="grid md:grid-cols-3 mt-8 gap-10">
            <Post :posts ="posts"/>
        </div>
    </section>
</template>