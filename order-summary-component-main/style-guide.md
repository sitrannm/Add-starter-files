@'
:root {
  --pale-blue: hsl(225, 100%, 94%);
  --bright-blue: hsl(245, 75%, 52%);
  --very-pale-blue: hsl(225, 100%, 98%);
  --desaturated-blue: hsl(224, 23%, 55%);
  --dark-blue: hsl(223, 47%, 23%);
  --white: hsl(0, 0%, 100%);
  --font: "Red Hat Display", sans-serif;
}

*,
*::before,
*::after {
  box-sizing: border-box;
  margin: 0;
  padding: 0;
}

body {
  min-height: 100vh;
  display: flex;
  flex-direction: column;
  background-color: var(--pale-blue);
  background-image: url("./images/pattern-background-mobile.svg");
  background-repeat: no-repeat;
  background-position: top center;
  background-size: 100% auto;
  font-family: var(--font);
  font-size: 1rem;
  font-weight: 500;
  color: var(--desaturated-blue);
}

img {
  display: block;
  max-width: 100%;
}

.page {
  flex: 1;
  display: grid;
  align-items: start;
  justify-items: center;
}

.summary {
  width: 100%;
  max-width: 28.125rem;
  overflow: hidden;
  background-color: var(--white);
  border-radius: 0 0 1.25rem 1.25rem;
}

.summary__hero {
  width: 100%;
  height: auto;
}

.summary__body {
  padding: 2rem 1.5rem;
  text-align: center;
}

.summary__title {
  margin-bottom: 1rem;
  font-size: 1.75rem;
  font-weight: 900;
  color: var(--dark-blue);
}

.summary__text {
  margin-bottom: 1.5rem;
  line-height: 1.6;
}

.plan {
  display: flex;
  align-items: center;
  gap: 1.25rem;
  margin-bottom: 1.5rem;
  padding: 1.25rem 1.5rem;
  background-color: var(--very-pale-blue);
  border-radius: 0.75rem;
  text-align: left;
}

.plan__icon {
  flex-shrink: 0;
}

.plan__info {
  flex: 1;
}

.plan__name {
  font-weight: 700;
  color: var(--dark-blue);
}

.plan__price {
  color: var(--desaturated-blue);
}

.plan__change {
  font-weight: 700;
  color: var(--bright-blue);
  text-decoration: underline;
}

.plan__change:hover {
  color: hsl(245, 75%, 72%);
  text-decoration: none;
}

.btn {
  display: block;
  width: 100%;
  margin-bottom: 1.5rem;
  padding: 1rem;
  border: 0;
  border-radius: 0.625rem;
  background-color: var(--bright-blue);
  box-shadow: 0 1rem 1.5rem hsla(245, 75%, 52%, 0.3);
  color: var(--white);
  font-family: inherit;
  font-size: 1rem;
  font-weight: 700;
  cursor: pointer;
  transition: opacity 0.2s ease;
}

.btn:hover {
  opacity: 0.8;
}

.cancel {
  border: 0;
  background: none;
  color: var(--desaturated-blue);
  font-family: inherit;
  font-size: 1rem;
  font-weight: 700;
  cursor: pointer;
  transition: color 0.2s ease;
}

.cancel:hover {
  color: var(--dark-blue);
}

.btn:focus-visible,
.cancel:focus-visible,
.plan__change:focus-visible {
  outline: 3px solid var(--dark-blue);
  outline-offset: 3px;
}

.attribution {
  padding: 1rem;
  font-size: 0.6875rem;
  text-align: center;
}

.attribution a {
  color: var(--bright-blue);
}

@media (min-width: 600px) {
  body {
    background-image: url("./images/pattern-background-desktop.svg");
  }

  .page {
    align-items: center;
    padding: 1.5rem;
  }

  .summary {
    border-radius: 1.25rem;
    box-shadow: 0 2rem 3rem hsla(225, 40%, 60%, 0.2);
  }

  .summary__body {
    padding: 2.5rem;
  }
}

@media (prefers-reduced-motion: reduce) {
  .btn,
  .cancel {
    transition: none;
  }
}
'@ | Set-Content -Encoding utf8 style.css

dir style.css