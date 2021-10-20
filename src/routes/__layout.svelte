<script>
  import Icon from '../components/icon.svelte'
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
    <Icon width="36" height="36" name="lamp" class={darkMode ? 'light-fill' : 'dark-fill'} />
  </button>
</nav>

<slot></slot>

<style lang="scss">
  @import 'src/styles/layout.scss';
</style>