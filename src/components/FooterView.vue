<template>
  <v-footer>
    <v-card elevation="0" rounded="0" width="100%" class="bg-grey text-center">
      <v-card-text>
        <v-btn
          class="mx-4"
          icon="fas fa-comment"
          variant="plain"
          color="white"
        ></v-btn>
        <v-btn
          class="mx-4"
          icon="fas fa-university"
          variant="plain"
          color="white"
        ></v-btn>
        <v-btn
          class="mx-4"
          icon="fas fa-wifi"
          variant="plain"
          color="white"
        ></v-btn>
        <v-btn
          class="mx-4"
          icon="fas fa-podcast"
          variant="plain"
          color="white"
        ></v-btn>
        <v-row> </v-row>
      </v-card-text>
      <v-col cols="12" sm="4">
        <v-card-text class="pt-0">
          <v-btn class="mx-1" icon>
            <v-icon color="#134A5B">fa-solid fa-heart</v-icon>
          </v-btn>
          @ {{ new Date().getFullYear() }} —
          <strong>All Rights Reserved by Bilge KÖŞE</strong>
        </v-card-text>
      </v-col>
    </v-card>
  </v-footer>
</template>

<script>
export default {};
</script>

<style>
.v-footer {
  padding: 8px 0 !important;
}
</style>