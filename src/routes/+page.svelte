<div class="page-container px-8">
  <header>
    <nav class="py-4 font-medium">
      <a class="py-4 pr-4 uppercase text-[var(--header-text)]" href="#">about</a>
      <a class="py-4 pr-4 uppercase text-[var(--header-text)]" href="#">contact</a>
      <button class="py-2 px-8">Login</button>
    </nav>
  </header>
  <aside class="mt-10">
    <h2>Recent Posts</h2>
    <nav>
      <ul>
        {#each ['One', 'Two', 'Three', 'Four', 'Five'] as titlePlaceholder}
          <li><a href="#">Part {titlePlaceholder}</a></li>
        {/each}
      </ul>
    </nav>
  </aside>
  <main class="mb-12">
    <img src="/header.jpeg" alt="hero" />
    <article class="mt-6 space-y-4">
      <h1 class="text-4xl">Flexbox Layout</h1>
      <p>
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Doloremque praesentium temporibus
        fugiat in id voluptatibus consequatur hic fuga commodi quidem nemo, deserunt amet rem
        tempora dolores, incidunt harum perspiciatis reprehenderit?
      </p>
      <p>
        Lorem ipsum, dolor sit amet consectetur adipisicing elit. Repudiandae atque exercitationem
        ex a harum natus adipisci soluta inventore ut fuga in beatae accusamus suscipit laboriosam,
        totam sed dolor architecto! Tenetur.
      </p>
    </article>
  </main>
  <footer class="space-y-2 p-6">
    <h2 class="text-xl font-bold">Flexbox Layout Example</h2>
    <p class="font-medium text-black">Hope you enjoyed learning about Flexbox Layouts!</p>
  </footer>
</div>

<style>
  @import url('https://fonts.googleapis.com/css?family=Montserrat:400,500,600,700');
  :global(:root) {
    --white: #fff;
    --header-border: #b0e0ea;
    --header-text: #9f9c9c;
    --login-button: #51bb7b;
    --main-text-heading: #50c6db;
    --side-bar-border: #693f7e;
    --footer: #9f9c9c;
  }
  :global(body) {
    color: #434344;
    font-family: 'Montserrat', sans-serif;
    font-weight: 400;
  }

  header {
    border-bottom: solid 2px var(--header-border);
    grid-area: header;
  }
  header nav {
    display: flex;
    justify-content: flex-start;
    align-items: center;
  }
  header button {
    background: var(--login-button);
    border: none;
    border-radius: 4rem;
    color: var(--white);
    font-weight: 600;
    margin-left: auto;
  }
  aside {
    background-color: #f9f9f9;
    border-top: solid 3px var(--side-bar-border);
    grid-area: aside;
    padding-left: 2rem;
    padding-bottom: 1rem;
  }
  aside h2 {
    font-weight: bold;
    margin-top: 1rem;
    margin-bottom: 0.5rem;
  }
  main {
    grid-area: main;
  }
  article h1 {
    color: var(--main-text-heading);
    font-weight: bold;
  }
  footer {
    background: var(--footer);
    grid-area: footer;
    text-align: center;
  }
  footer h2 {
    color: white;
  }

  @screen sm {
    .page-container {
      display: grid;
      grid-template-areas: 'header header' 'aside main' 'footer footer';
    }
    aside {
      padding-left: 2rem;
      padding-right: 2rem;
    }
    aside h2 {
      margin: 0 auto;
      padding-right: auto;
      padding-top: 1rem;
    }
    main {
      margin-top: 2.5rem;
      margin-left: 2rem;
    }
    aside,
    main {
      margin-bottom: 4rem;
    }
  }
</style>
