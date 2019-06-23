<template>
  <div id="contact-section">
    <ContactButton
      text="gh"
      destination="https://github.com/coughinbach"
      :colorScheme="formatColorScheme('#ffa8e6', '#f4daed', '#d491c1')"
    />
    <ContactButton
      text="@"
      destination="mailto:lolabarbierhoffenbach@gmail.com"
      :colorScheme="formatColorScheme('#97d5f2', '#c4e3f2', '#7cb2cc')"
    />
    <ContactButton
      text="ig"
      destination="https://www.instagram.com/coughinbach/"
      :colorScheme="formatColorScheme('#f4b87a', '#f0d5b8', '#db9f62')"
    />
    <ContactButton
      text="li"
      destination="https://www.linkedin.com/in/lola-barbier/"
      :colorScheme="formatColorScheme('#90e7a8', '#b8f0c7', '#7ccc92')"
    />
  </div>
</template>

<script>
import ContactButton from './ContactButton.vue';

export default {
  name: 'ContactSection',
  components: { ContactButton },
  methods: {
    formatColorScheme(bg, highlight, shadow) {
      return {
        'borderLight': highlight,
        'borderShadow': shadow,
        'bg': bg,
      }
    },
  }
}
</script>

<style lang="scss">
#contact-section {
  margin-top: 20px;
  width: 200px;
  display: flex;
  justify-content: space-between;
}
</style>
