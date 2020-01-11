<script>
  import { createEventDispatcher } from 'svelte'
  const dispatch = createEventDispatcher()

  export let active
  export let book

  function onClickNav() {
    dispatch('navClicked', { book })
  }
</script>

<li class="nav-tab-list-el" class:active on:click="{ onClickNav }">
  <img class="book-thumb" src={ book.imgUrl }>
</li>

<style type="text/scss">
  .nav-tab-list-el {
    min-width: 100px;
    margin: 16px;
    opacity: 0.5;
    &.active {
      opacity: 1.0;
    }
    .book-thumb {
      height: 100px;
    }
  }
</style>
