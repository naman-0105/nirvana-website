<script>
  const events = [
    {
      name: "Bytes & Books Readathon",
      image: "BnB.png",
      description: "Bytes and Book Readathons, organized by Nirvana, bring together book lovers and tech enthusiasts for an exciting blend of reading challenges and tech exploration. Participants dive into diverse genres, share reviews, and engage in literary discussions, while also exploring coding, programming, and the latest tech trends. These events create a vibrant community, fostering learning, collaboration, and fun for all.",
      sponsors: ["Image1.jpg", "Image1.jpg"]
    },
    {
      name: "Bytes & Books Readathon",
      image: "BnB.png",
      description: "Bytes and Book Readathons, organized by Nirvana, bring together book lovers and tech enthusiasts for an exciting blend of reading challenges and tech exploration. Participants dive into diverse genres, share reviews, and engage in literary discussions, while also exploring coding, programming, and the latest tech trends. These events create a vibrant community, fostering learning, collaboration, and fun for all.",
      sponsors: ["Image1.jpg", "Image1.jpg"]
    },
    {
      name: "Bytes & Books Readathon",
      image: "BnB.png",
      description: "Bytes and Book Readathons, organized by Nirvana, bring together book lovers and tech enthusiasts for an exciting blend of reading challenges and tech exploration. Participants dive into diverse genres, share reviews, and engage in literary discussions, while also exploring coding, programming, and the latest tech trends. These events create a vibrant community, fostering learning, collaboration, and fun for all.",
      sponsors: ["Image1.jpg", "Image1.jpg"]
    },
  ];
</script>

<style>
  .about-container {
    font-family: Arial, sans-serif;
    padding: 20px;
    text-align: center;
    color: #333;
    background-color: #FFF9F5;
    ;;
  }

  .head {
    font-family: 'Krona One', sans-serif;
    font-size: 3rem;
    font-weight: 700;
    color: #2c3e50;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1);
    margin-bottom: 20px;
  }

  .about-container span {
    color: #FF6F00;
  }

  .subheading {
    font-size: 1.4rem;
    color: #666;
    margin-bottom: 70px;
  }

  .events-grid {
    display: grid;
    grid-template-columns: repeat(3, 1fr);
    gap: 40px;
    justify-items: center;
    margin: 40px auto;
    max-width: 1000px;
  }

  .event-card {
    perspective: 1000px;
    width: 280px;
    height: 400px;
  }

  .event-card-inner {
    position: relative;
    width: 100%;
    height: 100%;
    text-align: center;
    transform-style: preserve-3d;
    transform: rotateY(0);
    transition: transform 0.6s;
  }

  .event-card:hover .event-card-inner {
    transform: rotateY(180deg);
  }

  .event-card-front,
  .event-card-back {
    position: absolute;
    width: 100%;
    height: 100%;
    backface-visibility: hidden;
    border-radius: 10px;
    overflow: hidden;
    box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: flex-start;
    padding: 20px;
    box-sizing: border-box;
  }

  .event-card-front {
    background: #fff;
  }

  .event-card-back {
    background: #2c3e50;
    color: #fff;
    transform: rotateY(180deg);
  }

  .event-image {
    width: 226px;
    height: 320px;
    background-size: cover;
    background-position: center;
    border-radius: 10px;
    margin-bottom: 10px;
  }

  .event-name {
    font-size: 18px;
    font-weight: bold;
    color: #333;
    margin-top: 10px;
  }

  .event-description {
    font-size: 14px;
    color: #ddd;
    text-align: center;
    margin-bottom: 20px;
  }

  .sponsors-heading {
    font-size: 20px;
    font-weight: bold;
    margin-bottom: 10px;
    color: #FF6F00;
  }

  .sponsor-logos {
    display: flex;
    justify-content: center;
    gap: 10px;
  }

  .sponsor-logo {
    width: 100px;
    height: 100px;
    background-size: cover;
    background-position: center;
    border-radius: 5px;
  }

  @media (max-width: 768px) {
    .events-grid {
      grid-template-columns: repeat(2, 1fr);
    }
  }

  @media (max-width: 480px) {
    .events-grid {
      grid-template-columns: 1fr;
    }
  }
</style>

<div class="about-container">
  <h2 class="head">EXPLORE OUR <span>EVENTS</span></h2>
  <p class="subheading">
    From Hackathons to insightful talks and workshops, explore the transformative events organized by Nirvana!
  </p>

  <div class="events-grid">
    {#each events as event}
      <div class="event-card">
        <div class="event-card-inner">
          <!-- Front Side -->
          <div class="event-card-front">
            <div
              class="event-image"
              style="background-image: url({event.image});"
            ></div>
            <div class="event-name">{event.name}</div>
          </div>

          <!-- Back Side -->
          <div class="event-card-back">
            <div class="event-description">{event.description}</div>
            <div class="sponsors-heading">Sponsors</div>
            <div class="sponsor-logos">
              {#each event.sponsors as sponsor}
                <div
                  class="sponsor-logo"
                  style="background-image: url({sponsor});"
                ></div>
              {/each}
            </div>
          </div>
        </div>
      </div>
    {/each}
  </div>
</div>
