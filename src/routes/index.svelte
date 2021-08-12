<script>
  import Image from "svelte-image"
</script>

<svelte:head>
  <title>Home | bigspeed</title>
</svelte:head>
<div class="container">
  <div class="profile">
    <Image src="bigspeed.png" alt="bigspeed" sizes="(max-width: 250px) 27vw, 250px" />
  </div>
  <div class="text-container">
    <span class="hello">Hi! I'm <strong>Andrew</strong>.</span>
    <span class="subtitle">I'm a 16-year-old FPV drone pilot from North Carolina.</span>

    <div class="social-container">
      <a class="social-link" href="https://github.com/bigspeedfpv">
        <div class="social github">
          <img class="social-icon" src="/github.svg" alt="Github logo" />
          <span class="social-label">bigspeedfpv</span>
        </div>
      </a>

      <a class="social-link" href="https://www.youtube.com/channel/UCreBMQ7cWcrzdvrrBK1HaXQ">
        <div class="social youtube">
          <img class="social-icon" src="/youtube.svg" alt="YouTube logo" />
          <span class="social-label">bigspeed</span>
        </div>
      </a>

      <a class="social-link" href="https://instagram.com/bigspeedfpv">
        <div class="social instagram">
          <img class="social-icon" src="/instagram.svg" alt="Instagram logo" />
          <span class="social-label">bigspeedfpv</span>
        </div>
      </a>
    </div>
  </div>
</div>

<style>
  .container {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;

    padding: 25px;
    min-height: calc(100% - 50px);

    display: flex;
    align-items: center;
    justify-content: center;
    gap: 25px;
  }

  .profile {
    width: 250px;
    height: 250px;

    border-radius: 100%;
    overflow: hidden;

    object-fit: cover;

    filter: drop-shadow(0px 15px 25px rgba(0, 0, 0, 0.2));
  }

  .text-container {
    display: flex;
    align-items: center;
    justify-content: center;
    flex-direction: column;
    gap: 20px;
  }

  .hello {
    font-size: 60px;
    max-width: 500px;
    text-align: center;
  }

  .subtitle {
    font-size: 30px;
    max-width: 550px;
    text-align: center;
  }

  .social-container {
    display: flex;
    align-items: center;
    justify-content: center;
    gap: 20px;
    flex-wrap: wrap;
  }

  .social-link {
    all: inherit;
    margin: 0;
    cursor: pointer;
  }

  .social {
    display: flex;
    align-items: center;
    justify-content: center;

    color: white;
    font-weight: bold;
    font-size: 24px;

    border-radius: 10px;
    width: 100%;
  }

  .github {
    background-color: black;
  }

  .youtube {
    background-color: #ff0000;
  }

  .instagram {
    background-color: #E1306C;
  }

  .social-icon {
    height: 30px;
    filter: invert();

    margin: 10px;
  }

  .social-label {
    margin-right: 10px;
  }

  @media only screen and (max-width: 950px) {
    .container, .social-container {
      flex-direction: column;
    }

    .social-container {
      gap: 10px;
      padding: 5px;
    }
  }

  @media only screen and (prefers-color-scheme: dark) {
    .container {
      color: white;
      background-color: #121212;
    }

    .text-container {
      opacity: 87%;
    }

    .github {
      filter: invert();
    }
  }
</style>
