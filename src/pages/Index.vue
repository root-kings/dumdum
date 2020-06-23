<template>
  <q-page class="flex flex-center">
    <div class="column  items-center">
      <div class="col">
        <div class="text-h5 text-center q-ma-md">{{ compliment }}</div>
      </div>
      <div class="col q-my-lg">
        <q-btn round icon="favorite" color="red" @click="fetchCompliment" />
      </div>
    </div>
    <div class="fixed-bottom text-center q-py-md">
      <q-btn label="About" icon="info" flat color="blue" to="/about" />
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageIndex",
  data() {
    return {
      compliment: ""
    };
  },
  methods: {
    fetchCompliment() {
      this.$axios.get("https://complimentr.com/api").then(response => {
        this.compliment = response.data.compliment;
      });
    }
  },
  mounted() {
    this.fetchCompliment();
  }
};
</script>
