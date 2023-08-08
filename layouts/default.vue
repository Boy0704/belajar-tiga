<template>
    <div id="wrapper">
        <app-sidebar v-if="isAuth"></app-sidebar>
        <div id="content-wrapper" class="d-flex flex-column">
			<div id="content">
                <app-header v-if="isAuth"></app-header>
                <nuxt/>

            </div>
        </div>
    </div>
</template>

<script>
import SideBar from '../components/layouts/SideBar.vue';
import Header from '../components/layouts/Header.vue';

export default {
    data() {
        return {
            isAuth: false
        }
    },
    components: {
        'app-sidebar' : SideBar,
        'app-header' : Header
    }    
}
</script>