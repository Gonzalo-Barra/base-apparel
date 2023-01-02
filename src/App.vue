<template lang="">
  <article class="card">
    <figure class="logo">
      <img src="/images/logo.svg" alt="logo" />
    </figure>

    <section class="banner">
      <figure class="banner-mobile">
        <img src="/images/hero-mobile.jpg" alt="logo" />
      </figure>
      <figure class="banner-desktop">
        <img src="/images/hero-desktop.jpg" alt="logo" />
      </figure>
    </section>
    <section class="text">
      <h1>WE'RE<strong>COMING SOON</strong></h1>
      <p>
        Hello fellow shoppers! We're currently building our new fashion store.
        Add your email below to stay up-to-date with announcements and our
        launch deals.
      </p>
    </section>
  </article>
</template>
<script>
export default {};
</script>
<style>
.card {
  display: grid;
  grid-template-rows: 0.25fr 0.5fr 1fr;
  grid-auto-columns: 1fr;
  gap: 0px 0px;
  grid-auto-flow: row;
  grid-template-areas:
    "logo"
    "banner-mobile"
    "text";
}

.logo img {
  min-width: 100px;
  max-width: 250px;
  grid-area: logo;
  padding: 1.5rem 0 0 1.5rem;
}

.banner {
  grid-area: banner-mobile;
}
.banner-mobile img {
  width: 100%;
  height: 100%;
}

.banner-desktop {
  display: none;
}

.text {
  grid-area: text;
  display: flex;
  flex-direction: column;
  justify-content: center;
  align-items: center;
}

.text h1 {
  font-family: "Josefin Sans", sans-serif;
  font-size: 1.5rem;
  font-weight: 600;
  margin-bottom: 1rem;
  padding: 50px 20px;
}
.text p {
  font-family: "Josefin Sans", sans-serif;
  font-size: 1rem;
  padding: 0 1.125rem;
  text-align: center;
}

@media (min-width: 1440px) {
  .card {
    display: grid;
    grid-auto-columns: 1fr;
    grid-template-columns: 1.6fr 1fr;
    grid-template-rows: 0.3fr 2fr;
    gap: 0px 0px;
    grid-template-areas:
      "text banner-desktop"
      "text banner-desktop";
  }
  .text {
    grid-area: text;
    display: flex;
    flex-direction: column;

    justify-content: center;
    align-items: center;
    background-image: url("/images/bg-pattern-desktop.svg");
    background-repeat: no-repeat;
    background-position: center;
    background-size: cover;
    padding: 0 200px;
  }
  .banner {
    grid-area: banner-desktop;
  }

  .banner-mobile {
    display: none;
  }

  .banner-desktop {
    display: block;
    grid-area: banner-desktop;
  }
  .logo {
    grid-area: text;
    z-index: 1;
  }
}
</style>
