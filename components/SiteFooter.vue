<script setup>
    const links =[
        { name:'Github' , href:'http://github.com', icon: 'entypo-social:github'},
        { name:'500px' , href:'http://500px.com', icon: 'entypo-social:500px'},
        { name:'Instagram' , href:'http://instagram.com', icon: 'entypo-social:instagram'},
        { name:'Linkedin' , href:'http://linkedin.com', icon: 'entypo-social:linkedin'},
        { name:'Medium' , href:'http://medium.com', icon: 'entypo-social:medium'},
        { name:'Twitter' , href:'http://twitter.com', icon: 'entypo-social:twitter'},
    ]
</script>
<template>
    <footer class="bg-gray-800">
        <section class="mx-auto max-w-7xl px2 sm:px-4 lg:py-6 text-gray-300 flex flex-row">
            <p class="flex-1">Giuseppe Frattura 2023</p>
            <div class="flex flex-row justify-center gap-4 mb-4 mt-2">
                <a v-for="link in links" :key="link.name" :href="link.href">
                    <Icon :name="link.icon" size="1.5rem" class="text-gray-300" />
                </a>
            </div>
        </section>

    </footer>
        
</template>