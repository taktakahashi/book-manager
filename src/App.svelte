<script>
  let books = [
    { id: 1, name: 'ゼロから始めるデザインシステム', imgUrl: 'https://i.gyazo.com/a3ddad4c037aca4778628c826a64ce4c.jpg' },
    { id: 2, name: 'アスキーアート技術読本', imgUrl: 'https://i.gyazo.com/3992e2f40adb6706f9f187fe3c8843d4.jpg' },
    { id: 3, name: 'ポモドーロ GTD すきま時間予定表で目標達成する本', imgUrl: 'https://i.gyazo.com/0e69af4e7fd229fae9c6b6c44c9bb4d9.png' },
    { id: 4, name: 'Nuxt Svelte Ionicで作る爆速フロントエンド 3つの世界', imgUrl: 'https://i.gyazo.com/a5db257b7b48210536d387ba9ad5da80.jpg' }
  ]

  let showedBook = books[0]

</script>

<main>
  <section class="book">
    <div class="book-info">
      <img class="book-img" src={ showedBook.imgUrl }>
    </div>
  </section>
  <nav class="nav-tab">
    <ul class="nav-tab-list">
      { #each books as book (book.id) }
        <li class="nav-tab-list-el" class:active="{ book === showedBook }" on:click="{ () => showedBook = book }">
          <img class="book-thumb" src={ book.imgUrl }>
        </li>
      { /each }
    </ul>
  </nav>
</main>

<style type="text/scss">
  .nav-tab {
    .nav-tab-list {
      list-style-type: none;
      display: flex;
      justify-content: center;
      margin-bottom: 0;
      .nav-tab-list-el {
        min-width: 100px;
        margin: 16px 16px 0;
        opacity: 0.5;
        &.active {
          opacity: 1.0;
        }
        .book-thumb {
          height: 100px;
        }
      }
    }
  }
  .book {
    .book-info {
      height: 400px;
      display: flex;
      justify-content: center;
      margin-top: 32px;
      .book-img {
        height: 100%;
      }
    }
  }
</style>
