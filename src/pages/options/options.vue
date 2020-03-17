<template>
  <div>
    <header>
      <h3>{{ i18n('general_settings', 'General settings') }}</h3>
      <p>{{ i18n('general_settings_hint', 'Change the behavior of the switcher to best fit your needs.') }}</p>
    </header>

    <main class="block switches-at-left">
      <section>
        <div class="left">
          <ios-checkbox id="extension-enabled" value="extensionEnabled" v-model="checked" />
        </div>
        <div class="right">
          <label for="extension-enabled">
            {{ i18n('enable_switcher', 'Enable Agent switcher') }}
          </label>
        </div>
        <div class="clear"></div>
      </section>
    </main>

    <footer>

    </footer>
  </div>
</template>

<script lang="ts">
import Vue from 'vue';

import IosCheckbox from '@/pages/components/ios-checkbox.vue';

import i18nMixin from '@/pages/mixins/i18n';

export default Vue.extend({
  components: { IosCheckbox },
  mixins: [i18nMixin],
  data() {
    return {
      checked: []
    };
  },
});
</script>

<style lang="scss" scoped>
p {
  font-size: 20px;
}
</style>
