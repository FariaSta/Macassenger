<template>
  <button class="ButtonFocus">
      <slot />
  </button>
</template>

<style scoped>

    .ButtonFocus
    {
        width: 143px;
        height: 47px;
        border-radius: 10px;
        background: #7BC411;
        color: white;
        border: none;
        font-size: 20px;
    }


</style>