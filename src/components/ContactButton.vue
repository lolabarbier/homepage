<template>
  <button v-bind:style="setColors" class="contact-button" @click="handleClick">
    {{ text }}
  </button>
</template>

<script>

export default {
  name: 'ContactButton',
  props: {
    text: {
      type: String,
      required: true,
    },
    destination: {
      type: String,
      required: true,
    },
    colorScheme: {
      type: Object,
      required: true,
    },
  },
  computed: {
    setColors() {
      if (this.colorScheme === {}) return '';
      return `background: ${this.colorScheme.bg};
        border-top: 5px solid ${this.colorScheme.borderLight};
        border-left: 5px solid ${this.colorScheme.borderLight};
        border-bottom: 5px solid ${this.colorScheme.borderShadow};
        border-right: 5px solid ${this.colorScheme.borderShadow};`;
    },
  },
  methods: {
    handleClick() {
      window.location.href = this.destination;
    }
  }
}
</script>

<style lang="scss">
.contact-button {
  padding: 2px 8px;
  color: white;
  font-size: 12px;
  text-decoration: none;
  font-family: "Comic Sans MS", cursive, sans-serif;

  &:hover {
    text-decoration: underline;
  }

  &:active {
    transform: translateY(2px) translateX(2px);
  }
}
</style>
