<script>
  import Heading from "$lib/organisms/Heading.svelte";
  let { title, content } = $props();
</script>

<section>
  <div class="pin"></div>
  <div>
    <Heading {title} />
    {@html content.html}
  </div>
</section>

<style>
  :root {
    --angle: 2.4deg;
    --count: 5;
    --duration: 1s;
    --delay: calc(-0.5 * var(--duration));
    --direction: alternate;
  }

  .pin {
    position: absolute;
    top: 10%;
    left: 50%;
    width: 0;
    height: 0;
    border-radius: 50%;
    transform: translate(-50%, -50%);
    z-index: 1000;
    background-color: var(--lavender);
  }

  section {
    position: relative;
    background-color: var(--grey);
    color: var(--blueberry);
    border-radius: var(--rounded) 0 0 0;
    height: 35rem;
    padding: 3rem 3rem 2rem 0rem;

    div {
      display: flex;
      flex-direction: column;
      justify-content: center;
      align-items: center;
      gap: 3rem;
      height: 30rem;
      padding: 1.25em;
      width: 100%;
      background-color: var(--white);
      border: 2px solid var(--turquoise);
      border-radius: var(--rounded);
      box-shadow: -4px 4px var(--lavender);

      animation-duration: var(--duration), 1.5s;
      animation-delay: var(--delay),
      calc(var(--delay) + var(--duration) * var(--count));
      animation-timing-function: ease-in-out;
      animation-iteration-count: var(--count), 1;
      animation-direction: var(--direction), normal;
      animation-fill-mode: both;
      animation-name: swing, swingEnd;
    }
  }

  @keyframes swing {
	0% {
		transform: rotate3d(0, 0, 1, calc(-1 * var(--angle)));
	}
	100% {
		transform: rotate3d(0, 0, 1, var(--angle));
	}
}
@keyframes swingEnd {
	to {
		transform: rotate3d(0, 0, 1, 0deg);
	}
}

  :global(section h2::selection, section p::selection) {
    background-color: var(--lavender);
    color: var(--lavender);
  }
  :global(section h2) {
    font-size: 2.25rem;
    padding: 0.25em;
    padding-left: 1rem;
  }
  :global(section p) {
    padding: 0 0.75em;
    font-size: 1.5rem;
    margin: 0;
    max-width: 65ch;
    letter-spacing: -0.04em;
  }
  @media (min-width: 750px) {
    div {
      width: max-content;
    }
  }
</style>
