<style>
  @import url('https://fonts.googleapis.com/css2?family=Krona+One&display=swap');
  
  :root {
    --primary: #FF6F00;
    --primary-light: #FFA040;
    --primary-dark: #C43E00;
    --text-dark: #2D2D2D;
    --background: #FFF9F5;
  }

  .about-page {
    font-family: 'Inter', sans-serif;
    line-height: 1.6;
    margin: 0 auto;
    padding: 40px 20px;
    max-width: 1000px;
    background: var(--background);
    opacity: 0;
    animation: fadeIn 1s ease-out forwards;
    position: relative;
    overflow: hidden;
    border-radius: 20px;
  }

  .content-wrapper {
    position: relative;
    z-index: 1;
  }

  .heading-container {
    text-align: center;
    margin-bottom: 50px;
    position: relative;
  }

  .heading {
    font-size: 3.5rem;
    font-weight: 800;
    color: black;
    margin-bottom: 30px;
    position: relative;
    display: inline-block;
    text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.1);
    opacity: 0;
    animation: slideDown 1s ease-out 0.3s forwards;
  }

  .head {
    font-family: 'Krona One', sans-serif;
    font-size: 3rem;
    font-weight: 700;
    color: #2c3e50;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1);
    position: relative;
    display: inline-block;
    margin-bottom: 10px;
    margin-top: 5px;
  }

  .head2 {
    font-family: 'Krona One', sans-serif;
    font-size: 2rem;
    font-weight: 600;
    color: #2c3e50;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1);
    position: relative;
    display: inline-block;
    margin-bottom: 5px;
    margin-top: 8px;
  }

  .heading-container span {
    color: #FF6F00;
  }

  .heading::before, .heading::after {
    content: '';
    position: absolute;
    height: 3px;
    width: 50px;
    top: 50%;
    animation: expandWidth 1s ease-out 1s forwards;
  }

  .heading::before {
    right: 120%;
    transform: translateX(50px);
  }

  .heading::after {
    left: 120%;
    transform: translateX(-50px);
  }

  @keyframes expandWidth {
    to { 
      width: 50px;
      transform: translateX(0);
    }
  }

  .section {
    background: white;
    padding: 40px;
    margin-bottom: 40px;
    box-shadow: 0 10px 30px rgba(255, 111, 0, 0.1);
    position: relative;
    overflow: hidden;
    border-radius: 15px;
  }

  .section::after {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    width: 100%;
    height: 100%;
    box-sizing: border-box;
  }

  .text {
    font-size: 1.2rem;
    color: var(--text-dark);
    margin-bottom: 30px;
    line-height: 1.8;
    opacity: 0;
    animation: fadeIn 1s ease-out 0.6s forwards;
  }

  .goals-list {
    list-style: none;
    padding: 0;
    display: flex;
    flex-direction: column;
    gap: 20px;
  }

  .goals-list li {
    background: white;
    padding: 25px;
    border-radius: 15px;
    box-shadow: 0 5px 15px rgba(255, 111, 0, 0.1);
    transition: all 0.3s ease;
    position: relative;
    overflow: hidden;
  }

  .goals-list li:hover {
    transform: translateY(-5px);
    box-shadow: 0 8px 25px rgba(255, 111, 0, 0.2);
  }

  @keyframes fadeIn {
    from { opacity: 0; transform: translateY(20px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @keyframes slideDown {
    from { opacity: 0; transform: translateY(-30px); }
    to { opacity: 1; transform: translateY(0); }
  }

  @media (max-width: 768px) {
    .heading {
      font-size: 2.5rem;
    }

    .section {
      padding: 25px;
    }
  }
</style>


<div class="about-page">
  <div class="content-wrapper">
    <div class="heading-container">
      <h1 class="heading head">WHO ARE <span>WE?</span></h1>
    </div>

    <div class="section">
      <p class="text">
        Nirvana is a vibrant community at IIIT Sri City, dedicated to empowering students
        through the fusion of ancient wisdom and modern knowledge. We bring together
        passionate individuals who are keen to explore the depths of traditional Indian
        Knowledge Systems while connecting them with contemporary sciences.
      </p>
      <p class="text">
        Our community is open to everyone, from students to professionals, who share an
        interest in meditation, yoga, and holistic well-being. Starting with a vision to
        help students lead balanced and successful lives, Nirvana has grown to host a
        variety of events including workshops, guest lectures, and reading sessions,
        fostering an environment of personal growth, knowledge sharing, and spiritual
        exploration.
      </p>
    </div>

    <div class="section">
      <div class="heading-container">
        <h4 class="heading head2">OUR GOALS</h4>

        <p class="text">
          At Nirvana, our primary goal is to empower individuals to lead balanced, successful lives by integrating ancient wisdom with modern knowledge.
      </p>
      <ul class="goals-list">
        <li>Promote Inner Well-being</li>
        <li>Foster Holistic Success</li>
        <li>Encourage Self-Discovery</li>
        <li>Facilitate Knowledge Sharing</li>
    </ul>
      </div>
    </div>
    
</div>
</div>
       
