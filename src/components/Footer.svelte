
<style>
  @import url('https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css');

  footer {
    text-align: center;
    padding: 40px 0;
    background-color: #f8f8f8;
    color: #333;
    font-family: Arial, sans-serif;
  }

  .footer-container {
    display: flex;
    justify-content: center;
    align-items: flex-start;
    flex-wrap: wrap;
    gap: 30px;
    padding: 0 20px;
    max-width: 1200px;
    margin: 0 auto;
  }

  .footer-column {
    flex: 1;
    min-width: 180px;
    text-align: center;
  }

  .footer-column h4 {
    margin-bottom: 15px;
    font-weight: bold;
    font-size: 1.2rem;
    color: #2c3e50;
  }

  .nirvana-description {
    margin-right: 100px;
    width: 350px;
    text-align: left;
  }

  .footer-column p,
  .footer-column a {
    margin: 8px 0;
    text-decoration: none;
    color: #555;
    font-size: 1rem;
  }

  .footer-column a:hover {
    text-decoration: underline;
    color: #FF6F00;
  }

  .footer-logo {
    width: 50px;
    height: auto;
    margin-right: 10px;
  }

  .social-media-icons {
    margin-top: 15px;
    display: flex;
    gap: 20px;
    justify-content: center;
  }

  .social-media-icons a {
    color: #555;
    font-size: 1.5rem;
    transition: color 0.3s ease;
  }

  .social-media-icons a:hover {
    color: #FF6F00;
  }

  .footer-bottom {
    font-size: 0.9rem;
    color: #666;
    margin-top: 20px;
    padding-top: 20px;
    border-top: 1px solid #ddd;
  }

  .footer-bottom p {
    margin: 0;
  }

  @media (max-width: 768px) {
    .footer-container {
      flex-direction: column;
      align-items: center;
      padding: 10px;
    }
    
    .nirvana-description {
      margin-right: 0;
      width: 100%;
      text-align: center;
      display: flex;
    flex-direction: column; 
    align-items: center; 
    justify-content: center;
    }

    .footer-column {
      text-align: center;
      margin-bottom: 20px;
    }

    .social-media-icons {
      gap: 30px;
      margin-top: 20px;
    }

    .footer-logo {
      width: 40px; 
      margin: 0 auto;
    }

    .footer-bottom {
      font-size: 0.8rem;
      padding: 10px 0;
    }
  }

  @media (max-width: 480px) {
    .footer-column h4 {
      font-size: 1rem;
    }

    .footer-column p,
    .footer-column a {
      font-size: 0.9rem;
    }

    .social-media-icons a {
      font-size: 1.2rem;
    }
  }
</style>

<footer>
  <div class="footer-container">
    <div class="footer-column nirvana-description">
      <div style="display: flex; align-items: center;">
        <img class="footer-logo" src="/NirvanaLogo.png" alt="Nirvana Logo" />
        <h4>NIRVANA</h4>
      </div>
      <p class="nirvana-description">
        A thriving community at IIIT Sri City dedicated to empowering students
        with overall well-being through adhyatma.
      </p>

      <div class="social-media-icons">
        <a href="https://discord.com/channels/1298283552819122197/1298303293092794378" target="_blank" title="Discord"><i class="fab fa-discord"></i></a>
        <a href="https://www.instagram.com/nirvana_iiits/" target="_blank" title="Instagram"><i class="fab fa-instagram"></i></a>
        <a href="https://www.linkedin.com/company/nirvana-iiits/" target="_blank" title="LinkedIn"><i class="fab fa-linkedin"></i></a>
      </div>
    </div>

    <!-- Events Section -->
    <div class="footer-column">
      <h4>Events</h4>
      <p><a href="#">Past Events</a></p>
      <p><a href="#">Upcoming Events</a></p>
    </div>

    <!-- Our Team Section -->
    <div class="footer-column">
      <h4>Our Team</h4>
      <p><a href="#">Alumnis</a></p>
      <p><a href="#">Members</a></p>
    </div>

    <!-- About Us Section -->
    <div class="footer-column">
      <h4>About Us</h4>
      <p><a href="#">Who are we?</a></p>
      <p><a href="#">Sponsors</a></p>
    </div>
  </div>

  <div class="footer-bottom">
    <p>Copyright © 2025 Nirvana IIITS. All Rights Reserved.</p>
  </div>
</footer>