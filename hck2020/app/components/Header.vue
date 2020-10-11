<template>
  <b-navbar class="nav" toggleable="sm" type="light" variant="light">
    <b-navbar-brand class="style='color: #555FFF'">PFreundschiff</b-navbar-brand>

    <b-nav-item class="styleForIwan" to="/">Events</b-nav-item>

    <b-nav-item-dropdown class="ml-auto" id="nav1" text="Sprache" right>
      <b-dropdown-item href="#">EN</b-dropdown-item>
      <b-dropdown-item href="#">ES</b-dropdown-item>
      <b-dropdown-item href="#">RU</b-dropdown-item>
      <b-dropdown-item href="#">FA</b-dropdown-item>
    </b-nav-item-dropdown>

    <b-nav-item-dropdown right>
      <template v-slot:button-content>
        <em> Menü </em>
      </template>
      <b-dropdown-item to="/NewEvent">Neues Event erstellen</b-dropdown-item>
      <b-dropdown-item href="#">Angemeldete Events</b-dropdown-item>
      <b-dropdown-item href="#">Benutzer</b-dropdown-item>
    </b-nav-item-dropdown>
  </b-navbar>
</template>
<style>
  .nav{
    background-color: #dddddd!important;
 }

</style>
