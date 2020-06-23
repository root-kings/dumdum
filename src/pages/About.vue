<template>
  <q-page class="flex flex-center">
    <div class="column  items-center">
      <div class="col">
        <div class="text-h5 text-center q-my-md">
          About Dumdum
        </div>

        <div class="text-body1 text-center q-ma-md">
          Dumdum is your personal complimentor. Get compliments whenever you're
          feeling low.
        </div>

        <div class="text-subtitle text-center q-my-md">
          Created with <q-icon name="favorite" color="red" /> by
          <a href="https://root-kings.github.io" target="_blank">Root Kings</a>.
        </div>
      </div>

      <div class="text-center q-py-md">
        <q-btn
          type="a"
          label="website"
          icon="info"
          flat
          color="blue"
          href="https://root-kings.github.io"
          target="_blank"
        />
      </div>
    </div>
  </q-page>
</template>

<script>
export default {
  name: "PageAbout"
};
</script>
