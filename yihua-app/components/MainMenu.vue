<template lang="pug">
  div
    b-nav
      b-nav-item(active) Home
      //- b-nav-item Link
      //- b-nav-item Another Link
      b-nav-item-dropdown.right
        template(slot="button-content") User
        b-dropdown-item(href="#") Profile
        b-dropdown-item(href="#") Signout
</template>