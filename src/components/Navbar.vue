<template>
    <nav>
        <v-toolbar flat app>
            <v-toolbar-side-icon class="grey--text" @click="drawer = !drawer"></v-toolbar-side-icon>
            <v-toolbar-title class="text-uppercase grey--text">
                <span class="font-weight-light">Todo</span>
                <span>Ninja</span>
            </v-toolbar-title>
            <v-spacer></v-spacer>
            <v-btn flat color="grey">
                <span>Sign Out</span>
                <v-icon right>exit_to_app</v-icon>
            </v-btn>
        </v-toolbar>

        <v-navigation-drawer app v-model="drawer" class="primary">
        <v-list-tile v-for="link in links" :key="link.text" router :to="link.route">
            <v-list-title-action>
                <v-icon class="white--text">{{ link.icon }}</v-icon>
            </v-list-title-action>
            <v-list-content>
                <v-list-tile-title class="white--text">{{ link.text }}</v-list-tile-title>
            </v-list-content>
        </v-list-tile>
        </v-navigation-drawer>

    </nav>
</template>

<script>
    export default {
      data() {
        return {
          drawer: false,
          links: [
            {icon: 'dashboard', text: 'Dashboard', route: '/'},
            {icon: 'folder', text: 'My Projects', route: '/projects'},
            {icon: 'person', text: 'Team', route: '/team'}
          ]
        }
      }
    }
</script>

<style></style>
