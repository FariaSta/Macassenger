<template>
  <button class="ButtonFocusLarge">
      <slot />
  </button>
</template>

<style scoped>

    .ButtonFocusLarge
    {
        width: 270px;
        height: 47px;
        border-radius: 10px;
        background: #7BC411;
        color: white;
        border: none;
        font-size: 20px;
    }


</style>