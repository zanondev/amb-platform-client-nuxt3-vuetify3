<template>
  <v-layout>
    <v-app-bar color="white" prominent>
      <v-spacer>
        <nuxt-link style="text-decoration: none" to="/">
          <v-icon
            class="btnHome"
            color="black"
            size="x-large"
            icon="mdi-home"
          ></v-icon>
        </nuxt-link>
      </v-spacer>
      <v-col cols="auto">
        <v-btn variant="text" class="btnSingIn" size="small" to="/login"
          >Entrar</v-btn
        >
      </v-col>
      <v-col cols="auto">
        <v-btn class="btnStartFree" block rounded="xl" size="small"
          >Começe grátis</v-btn
        >
      </v-col>
    </v-app-bar>
    <v-navigation-drawer app expand-on-hover rail>
      <v-divider></v-divider>

      <v-list density="compact" nav>
        <v-list-item
          prepend-icon="mdi-folder"
          title="My Files"
          value="myfiles"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-account-multiple"
          title="Clientes"
          value="shared"
          to="/customers/customerclients/clients"
        ></v-list-item>
        <v-list-item
          prepend-icon="mdi-star"
          title="Starred"
          value="starred"
        ></v-list-item>
      </v-list>
    </v-navigation-drawer>

    <v-main style="height: 250px"></v-main>
  </v-layout>
</template>

<style>
.btnStartFree {
  background: #5d8d49;
  color: #ffff;
  font-weight: bold;
}

.v-layout {
  height: 0 !important;
}

.v-btn--variant-contained::before {
  box-shadow: 0px 3px 1px -2px rgb(0 0 0 / 20%),
    0px 2px 2px 0px rgb(0 0 0 / 14%), 0px 1px 5px 0px rgb(0 0 0 / 12%);
}
.btnHome {
  padding-left: 1em;
}
</style>