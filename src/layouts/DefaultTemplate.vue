<template>
    <div>
        <header-component/>

        <section>
            <router-view></router-view>
        </section>

        <footer-component/>
    </div>
</template>

<script>
import HeaderComponent from './components/HeaderComponent.vue';
import FooterComponent from './components/FooterComponent.vue';
import { onBeforeMount } from '@vue/runtime-core';

export default {
   name: 'DefaultTemplate',
   setup() {
        onBeforeMount(() => {
            document.body.classList.add('page')
            document.body.classList.add('dark')

            document.title = 'EAD'
        })
   },
   components: {
        HeaderComponent,
        FooterComponent
   }
}
</script>