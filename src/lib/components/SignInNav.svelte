<script>
  import Logo from '$lib/ui/PrimoLogo.svelte'

  import { show } from '$lib/components/Modal.svelte'
</script>

<header role="navigation" aria-label="main navigation">
  <div class="logo">
    <Logo />
  </div>
  <nav>
    <button class="link" on:click={() => show('INVITE_COLLABORATORS')}
      >Invite Collaborators</button
    >
    <button class="link" on:click={() => show('USER_SETTINGS')}>Settings</button
    >
    <a class="link" href="https://docs.primo.af">
      <span>Docs</span>
      <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 512 512"
        ><path
          fill="currentColor"
          d="M432,320H400a16,16,0,0,0-16,16V448H64V128H208a16,16,0,0,0,16-16V80a16,16,0,0,0-16-16H48A48,48,0,0,0,0,112V464a48,48,0,0,0,48,48H400a48,48,0,0,0,48-48V336A16,16,0,0,0,432,320ZM474.67,0H316a28,28,0,0,0-28,28V46.71A28,28,0,0,0,316.79,73.9L384,72,135.06,319.09l-.06.06a24,24,0,0,0,0,33.94l23.94,23.85.06.06a24,24,0,0,0,33.91-.09L440,128l-1.88,67.22V196a28,28,0,0,0,28,28H484a28,28,0,0,0,28-28V37.33h0A37.33,37.33,0,0,0,474.67,0Z"
        /></svg
      >
    </a>
  </nav>
</header>

<style lang="postcss">
  header {
    display: flex;
    justify-content: space-between;
    align-items: center;
    color: var(--color-gray-3);
    margin-bottom: 1rem;

    .logo {
      width: 7rem;
    }

    .link {
      border-bottom: 2px solid transparent;
      display: flex;

      svg {
        width: 0.5rem;
        margin-left: 0.5rem;
      }
      &:hover {
        border-color: var(--primo-color-primored);
      }
    }

    nav {
      display: flex;
      align-items: center;
      gap: 1rem;

      .link {
        margin-right: 1rem;
      }
    }
  }

  .button {
    padding: 0.5rem 1rem;
    border: 1px solid var(--color-gray-7);
    border-radius: var(--primo-border-radius);

    &:hover {
      box-shadow: var(--primo-ring-primored);
    }
  }
</style>
