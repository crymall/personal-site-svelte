<script>
  let darkMode = false;

  const toggleDarkMode = () => {
    darkMode = !darkMode;
    const body = document.querySelector('body');
    body.className = darkMode ? 'dark-mode' : '';
  };
</script>

<nav class="topnav">
  <div class="leftside">
    <a href="/">home</a>
    <a href="/about">about</a>
  </div>
  <button on:click={toggleDarkMode}>
    toggle dark mode
  </button>
</nav>

<slot></slot>

<style lang="scss">
  @import 'src/styles/layout.scss';
</style>