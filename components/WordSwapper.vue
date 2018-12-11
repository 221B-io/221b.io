<template>
<section>
  <div class="text-left">
    <span>
        A consulting group <br>for when you need it to be
    </span>
    <span class="mb-0 changing-word">
      <Textra :data='["quick","beautiful","scalable", "accessible"]' :infinite="true" :timer="1" filter="simple" />
    </span>
  </div>
</section>
</template>
<script>
import Textra from '~/components/Textra';
export default {
  name: 'WordSwapper',
  components: {
    Textra
  }
};
</script>
<style>
.changing-word {
  /* border-bottom: 2px solid white; */
}
</style>
