<template>
  <q-page class="flex flex-center">
    {{ compliment }}
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
  mounted(){
    this.fetchCompliment()
  }
};
</script>
