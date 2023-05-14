<template>
  <div>
    <h1>This is {{ subdomain }}'s subdomain.</h1>
  </div>
</template>

<script>
export default {
  data() {
    return {
      subdomain: '',
    };
  },
  mounted() {
    this.subdomain = this.getSubdomain();
  },
  methods: {
    getSubdomain() {
      const hostname = window.location.hostname;
      const parts = hostname.split('.');
      if (parts.length > 2) {
        // Subdomain exists
        return parts[0];
      } else {
        // No subdomain
        return null;
      }
    },
  },
};
</script>
