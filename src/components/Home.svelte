<script>
  import { onMount } from 'svelte';
  import Typed from 'typed.js';
  let typed;

  onMount(() => {
    typed = new Typed('.tagline', {
      strings: [
        "Discover Inner Peace and Outer Success",
        "Unveil the Mysteries of Life",
        "Find Balance Through Meditation and Yoga",
        "Connect Ancient Wisdom with Modern Knowledge"
      ],
      typeSpeed: 60,
      backSpeed: 40,
      backDelay: 1500,
      loop: true,
      showCursor: false
    });
  });
</script>

<style>
  /* Base styles */
  :root {
    --primary: #FF6F00;
    --primary-light: #FFA040;
    --primary-dark: #C43E00;
    --text-dark: #2D2D2D;
    --background: #FFF9F5;
  }

  .home-container {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    text-align: center;
    padding: 20px;
    background: var(--background);
    position: relative;
    overflow: hidden;
  }

  .glitch {
    font-family: 'Krona One', sans-serif;
    font-size: 4rem;
    font-weight: 700;
    color: #2c3e50;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1);
    position: relative;
    display: inline-block;
    margin-bottom: 10px;
    margin-top: 5px;
  }

  .glitch span {
    color: var(--primary);
  }

  .tagline {
    font-size: 1.6rem;
    font-weight: 400;
    color: #343332;
    margin-top: 15px;
    white-space: nowrap;
    text-align: center;
  }

  .content-section {
    display: flex;
    justify-content: center;
    align-items: center;
    gap: 20px;
    margin-top: 30px;
  }

  .content-image {
    width: 600px;
    height: 400px;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    object-fit: cover;
    transition: all 0.3s ease;
  }

  .content-image.small {
    width: 350px;
    height: 320px;
  }

  .about-section {
    display: flex;
    align-items: flex-start;
    gap: 20px;
    margin-top: 150px;
    padding: 40px;
    flex-wrap: wrap;
  }

  .about-text {
    flex: 1;
    font-size: 16px;
    color: #333;
    line-height: 1.6;
    margin-left: 20px;
    text-align: left;
  }

  .about-text h2 {
    font-family: "Krona One", sans-serif;
    font-size: 2rem;
    margin-bottom: 20px;
    color: #2c3e50;
  }

  .about-text p {
    font-size: 1.1rem;
    margin-bottom: 20px;
  }

  .about-text ul {
    padding-left: 20px;
  }

  .about-text li {
    margin-bottom: 10px;
  }

  .about-video {
    width: 50%;
    height: 500px;
    border-radius: 10px;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  }

  .discord-button {
    margin-top: 30px;
    padding: 10px 20px;
    background-color: #FF6F00;
    color: #fff;
    border: none;
    border-radius: 5px;
    cursor: pointer;
    font-size: 20px;
    margin-bottom: 80px;
  }

  .discord-button:hover {
    background-color: #e65c00;
  }

  @media (max-width: 1024px) {
    .content-section {
      gap: 15px;
    }

    .content-image {
      width: 500px;
      height: 350px;
    }

    .content-image.small {
      width: 300px;
      height: 250px;
    }

    .about-video {
      height: 400px;
    }
  }

  @media (max-width: 768px) {
    .content-section {
      gap: 10px;
    }

    .content-image {
      width: 400px;
      height: 300px;
    }

    .content-image.small {
      width: 250px;
      height: 200px;
    }

    .about-section {
      flex-direction: column;
    }

    .about-video {
      width: 100%;
      height: 300px;
    }
  }

  @media (max-width: 480px) {
    .glitch {
      font-size: 2rem;
    }

    .tagline {
      font-size: 1.2rem;
    }

    .content-section {
      flex-direction: column;
      gap: 10px;
    }

    .content-image {
      width: 300px;
      height: 250px;
    }

    .content-image.small {
      width: 200px;
      height: 150px;
    }

    .about-section {
      padding: 20px;
    }
  }
</style>

<div class="home-container">
  <div class="mandala-bg"></div>
  <h1 class="welcome-heading">
    <p class="glitch">Welcome to <span>NIRVANA</span></p>
  </h1>
  <span class="subheading tagline"></span>

  <div class="content-section">
    <img class="content-image small" src="Image1.jpg" alt="Peaceful Nature" />
    <img class="content-image" src="Image1.jpg" alt="Meditation" />
    <img class="content-image small" src="Image1.jpg" alt="Yoga Session" />
  </div>

  <div class="about-section">
    <div class="about-video">
      <iframe 
        width="100%" 
        height="100%" 
        src="https://www.youtube.com/embed/uxIzvZzt6gU?si=HkpWi6Yvrg2Ytoo4" 
        title="YouTube video player" 
        frameborder="0" 
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" 
        allowfullscreen>
      </iframe>
    </div>

    <div class="about-text">
      <h2>About Nirvana</h2>
      <p>
        Nirvana at IIIT Sri City blends ancient wisdom with modern knowledge to inspire personal growth. 
        With a focus on mindfulness, yoga, and literary events like the “Books & Bytes Readathon,” Nirvana offers
        an enriching journey that fosters self-discovery and a deeper understanding of life’s purpose.
      </p>

      <h3>Our Mission</h3>
      <p>Our mission is to bridge the gap between mind, body, and spirit, helping individuals find balance through:</p>
      <ul>
        <li>Yoga and meditation practices</li>
        <li>Mindfulness workshops</li>
        <li>Engaging discussions and events</li>
      </ul>
    </div>
  </div>

  <button class="discord-button">Join Us On The Discord Server</button>
</div>
