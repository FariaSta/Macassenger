<template>
  <button class="ButtonNotFocus">
      <slot />
  </button>
</template>

<style scoped>

    .ButtonNotFocus
    {
        width: 143px;
        height: 47px;
        border-radius: 10px;
        background: none;
        color: white;
        border: 2px solid #7BC411;
        font-size: 20px;
        text-decoration: none;
    }


</style>