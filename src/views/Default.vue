<template>
  <v-layout class="align-center justify-center d-flex">
    <v-card width="600">
      <v-card-title class="daily">
        <h2 class="headline">Daily-log</h2>
        <h2 class="headline mt-4">How do you feel ?</h2>
      </v-card-title>
      <v-card-text>
        <v-container fluid>
          <v-textarea
            counter
            label="Text"
            :rules="rules"
            v-model="value"
          ></v-textarea>
        </v-container>
        <h2 class="headline">Rate your day</h2>
        <div class="d-flex align-center justify-center flex-column">
          <v-rating
            v-model="rating"
            color="yellow"
            class="ma-2"
            :item-labels="['sad', '', '', '', 'happy']"
            item-label-position="top"
          ></v-rating>
          <v-btn variant="tonal">
             Submit
          </v-btn>
        </div>
      </v-card-text>
    </v-card>
  </v-layout>
</template>

<script>
export default {
  data() {
    return {
      value: '',
      rating: 0,
      rules: [] 
    };
  }
};
</script>
