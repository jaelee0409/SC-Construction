<template>
    <v-app>
        <v-toolbar fixed app id="mainNav">
            <v-toolbar-title v-text="title" class="font-weight-bold"></v-toolbar-title>
            <v-spacer />
            <v-toolbar-items class="hidden-sm-and-down">
                <v-btn flat v-for="link in links" :key="link.name" :to="link.route" class="font-weight-bold" id="navItem">
                    {{ link.name }}
                </v-btn>
            </v-toolbar-items>

            <v-menu light class="hidden-md-and-up">
                <v-toolbar-side-icon slot="activator"></v-toolbar-side-icon>
                <v-list>
                    <v-list-tile v-for="link in links" :key="link.name" :to="link.route">
                         <v-list-tile-content>
                            <v-list-tile-title>{{ link.name }}</v-list-tile-title>
                        </v-list-tile-content>
                    </v-list-tile>   
                </v-list>
            </v-menu>
        </v-toolbar>
        <v-content class="pa-0">
            <nuxt />
        </v-content>
    </v-app>
</template>

<script>
export default {
    data() {
        return {
            title: 'SC Construction',
            links: [
                { name: 'Home', route: '/', id: 'navItem0' },
                { name: 'About', route: '/about', id: 'navItem1' },
                { name: 'Projects', route: '/projects', id: 'navItem2' },
                { name: 'Contact', route: '/contact', id: 'navItem3' },
            ]
        }
    }
}
</script>

<style>
#mainNav {
    background-color: rgba(255, 255, 255, 0.9);
}

#navItem:hover {
    color: #00818E;
}

#navItem.v-btn--active {
    color: #00818E;
}
</style>
