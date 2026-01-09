<template>
  <footer id="links">
    <ul>
      <li>
        <a href="mailto:alex.berneau@outlook.com">email</a>
      </li>
      <li>
        <a href="https://github.com/nothaldir" target="_blank" rel="noopener noreferrer">
          github
        </a>
      </li>
      <li>
        <a href="https://www.linkedin.com/in/alexberneau/" target="_blank" rel="noopener noreferrer">
          linkedIn
        </a>
      </li>
    </ul>
  </footer>
</template>

<style scoped>
footer {
  margin-top: 3rem;
  font-size: 0.8rem;
}

ul {
  display: flex;
  list-style-type: none;
  padding: 0;

  li+li {
    margin-left: 1rem;
  }

  a {
    color: inherit;
    text-decoration: none;
    position: relative;

    &::after {
      content: '';
      position: absolute;
      bottom: 0;
      left: 0%;
      width: 100%;
      height: 1px;
      background: var(--color-text);
      transform: scaleX(0);
      transform-origin: 0% 50%;
      transition: 0.2s cubic-bezier(0.4, 0, 0.2, 1);
    }

    &:hover {
      &::after {
        transform: scaleX(1);
      }
    }
  }
}
</style>
