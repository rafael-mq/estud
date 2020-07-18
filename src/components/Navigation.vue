<template>
  <div>
    <v-navigation-drawer
      app
      v-model="drawer"
      class="indigo lighten-1"
      dark
      disable-resize-watcher
    >
      <v-list>
        <v-list-item>
          <v-list-item-avatar>
            <v-img src="https://randomuser.me/api/portraits/men/78.jpg"></v-img>
          </v-list-item-avatar>

          <v-list-item-content>
            <v-list-item-title>John Leider</v-list-item-title>
          </v-list-item-content>
        </v-list-item>

        <v-divider></v-divider>

        <v-list dense>
          <v-list-item v-for="item in items" :key="item.title" link>
            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>

        <v-divider></v-divider>

        <v-list dense>
          <v-subheader>ALUNO</v-subheader>
          <v-list-item v-for="item in specificItems" :key="item.title" link>
            <v-list-item-icon>
              <v-icon v-text="item.icon"></v-icon>
            </v-list-item-icon>
            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-list>
    </v-navigation-drawer>

    <v-app-bar app color="indigo darken-1" dark>
      <v-app-bar-nav-icon
        class="hidden-md-and-up"
        @click="drawer = !drawer"
      ></v-app-bar-nav-icon>
      <v-spacer class="hidden-md-and-up"></v-spacer>
      <v-toolbar-title class="display-2 font-weight-bold">
        {{ appTitle }}
      </v-toolbar-title>
      <v-spacer></v-spacer>
      <v-btn
        elevation="0"
        color="indigo darken-1"
        class="hidden-sm-and-down ml-4"
        >Sobre</v-btn
      >
      <v-btn
        elevation="0"
        color="indigo darken-1"
        class="hidden-sm-and-down ml-4"
        >Login</v-btn
      >
      <v-btn color="indigo lighten-2" class="hidden-sm-and-down ml-4"
        >Cadastre-se</v-btn
      >
    </v-app-bar>
  </div>
</template>

<script>
export default {
  name: "Navigation",
  data() {
    return {
      appTitle: "Estud",
      drawer: null,
      items: [
        {
          title: "Login"
        },
        {
          title: "Cadastre-se"
        },
        {
          title: "Sobre"
        }
      ],
      specificItems: [
        { title: "Busca", icon: "mdi-magnify" },
        { title: "Aulas", icon: "mdi-book-open-variant" }
      ]
    };
  }
};
</script>

<style scoped></style>
