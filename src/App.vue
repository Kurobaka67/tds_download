<script>
export default {
  methods: {
    downloadAPK() {
      // create element <a> for download PDF
      const link = document.createElement('a');
      link.href = 'assets/app-release.apk';
      link.target = '_blank';
      link.download = 'app-release.apk';

      // Simulate a click on the element <a>
      document.body.appendChild(link);
      link.click();
      document.body.removeChild(link);
    }
  }
}
</script>

<template>
  <main>
    <button @click="downloadAPK">Clique pour télécharger</button>
  </main>
</template>

<style scoped>
header {
  line-height: 1.5;
}

.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
}
</style>
