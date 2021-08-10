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
    </div>
  </div>
</div>

<style>
  .container {
    position: fixed;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;

    padding: 25px;

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
    gap: 40px;
    padding: 10px;


  }

  .social-link {
    text-decoration: inherit;
    color: inherit;
  }

  .social {
    display: flex;
    gap: 10px;
    padding: 10px;
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

  .social-icon {
    height: 30px;
    filter: invert();
  }

  @media only screen and (max-width: 898px) {
    .container, .social-container {
      flex-direction: column;
    }
    
    .social-container {
      gap: 20px;
    }
  }
</style>
