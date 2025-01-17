<script>
  let members = [
    {
      name: "Himanshu Saraswat",
      role: "Lead",
      image: "Image1.jpg",
      email: "himanshu@example.com",
    },
    {
      name: "Naman Goyal",
      role: "Tech",
      image: "Image1.jpg",
      email: "naman@example.com",
    },
    {
      name: "Gaurav Gautam",
      role: "Tech",
      image: "Image1.jpg",
      email: "gaurav@example.com",
    },
    {
      name: "Vedant Kesarwani",
      role: "Design & Video",
      image: "Image1.jpg",
      email: "vedant@example.com",
    },
    {
      name: "Shyam Modi",
      role: "Research",
      image: "Image1.jpg",
      email: "shyam@example.com",
    },
    {
      name: "Dhruv Patel",
      role: "Research",
      image: "Image1.jpg",
      email: "dhruv@example.com",
    },
    {
      name: "Aashutosh Sinha",
      role: "Management",
      image: "Image1.jpg",
      email: "aashutosh@example.com",
    },
    {
      name: "Aadi Patel",
      role: "Management",
      image: "Image1.jpg",
      email: "aadi@example.com",
    },
    {
      name: "Vyom Nikhra",
      role: "Public Relations",
      image: "Image1.jpg",
      email: "vyom@example.com",
    },
    {
      name: "Siddharth Singh",
      role: "Public Relations",
      image: "Image1.jpg",
      email: "siddharth@example.com",
    }
  ];
</script>

<div class="container">
  <h1 class="heading head">MEET THE <span>TEAM</span></h1>
  <p class="subheading">One Vision, Many Minds, Infinite Possibilities.</p>

  <div class="members-container">
    {#each members as member}
      <div class="card">
        <div class="profile-pic">
          <img src={member.image} alt={member.name} />
        </div>
        <div class="content">
          <h3 class="name">{member.name}</h3>
          <p class="role">{member.role}</p>
          <div class="details">
            <p class="email">{member.email}</p>
          </div>
        </div>
      </div>
    {/each}
  </div>
</div>

<style>


  .container {
    width: 100%;
    max-width: 100vw;
    padding: 50px;
    text-align: center;
    min-height: 100vh;
    box-sizing: border-box;
    margin-bottom: 30px;
    background-color: #FFF9F5;

  }

  .container span {
    color: #FF6F00;
  }

  .heading {
    font-size: 36px;
    font-weight: bold;
    margin-bottom: 10px;
  }

  .head {
    font-family: 'Krona One', sans-serif;
    font-size: 3rem;
    font-weight: 700;
    color: #2c3e50;
    text-shadow: 2px 2px 5px rgba(0, 0, 0, 0.1);
    margin-bottom: 20px;
  }

  .subheading {
    font-size: 25px;
    color: #555;
    margin-bottom: 40px;
  }

  .content p.email {
    color: rgb(76, 76, 210);
  }

  .content h3.name {
    font-size: 16px;
    font-weight: 400;
  }

  .members-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-evenly;
    gap: 40px;
    margin-top: 120px;
    margin-bottom: 100px;
  }

  .card {
    position: relative;
    width: 185px;
    height: 180px;
    background-color: #fff;
    border-radius: 15px;
    box-shadow: 0 5px 15px rgba(0, 0, 0, 0.2);
    overflow: visible;
    text-align: center;
    transition: 0.3s ease-in-out;
    margin: 20px 40px;
  }

  .card:hover {
    height: 190px;
  }

  .card:hover .profile-pic {
    transform: translate(-50%, -20%);
  }

  .card:hover .content p.email {
    transform: translate(0%, -80%);
  }

  .card:hover .content h3.name {
    transform: translate(0%, -120%);
    transition: 0.3s ease-in-out;
  }

  .content h3.name {
    font-weight: 600;
  }

  .card:hover .content p.role {
    transform: translate(0%, -120%);
    transition: 0.3s ease-in-out;
  }

  .profile-pic {
    position: absolute;
    top: -40px;
    left: 50%;
    transform: translateX(-50%);
    width: 160px;
    height: 160px;
    border: 1px solid #fff;
    border-radius: 10%;
    overflow: hidden;
    box-shadow: 0 5px 10px rgba(0, 0, 0, 0.2);
    transition: transform 0.3s ease-in-out;
    z-index: 1;
  }

  .profile-pic img {
    width: 100%;
    height: 100%;
    object-fit: cover;
  }

  .content {
    margin-top: 120px;
    padding: 7px;
  }

  .content h3 {
    font-size: 18px;
    font-weight: bold;
    color: #111;
    margin: 5px 0;
  }

  .content p {
    font-size: 14px;
    color: #555;
    margin: 2px 0;
  }

  .details {
    visibility: hidden;
    opacity: 0;
    transform: translateY(20px);
    transition: 0.3s ease-in-out;
  }

  .card:hover .details {
    visibility: visible;
    opacity: 1;
    transform: translateY(0);
  }

  @media (max-width: 1024px) {
    .members-container {
      gap: 30px;
    }

    .card {
      width: 185px;
      height: 180px;
    }

    .profile-pic {
      width: 160px;
      height: 160px;
    }

    .heading {
      font-size: 30px;
    }

    .subheading {
      font-size: 22px;
    }
  }

  @media (max-width: 768px) {
    .members-container {
      gap: 25px;
      margin-top: 80px;
    }

    .card {
      width: 185px;
      height: 180px;
    }

    .profile-pic {
      width: 160px;
      height: 160px;
    }

    .heading {
      font-size: 26px;
    }

    .subheading {
      font-size: 20px;
    }
  }

  @media (max-width: 480px) {
    .members-container {
      gap: 15px;
      margin-top: 60px;
    }

    .card {
      width: 185px;
      height: 180px;
    }

    .profile-pic {
      width: 160px;
      height: 160px;
    }

    .heading {
      font-size: 22px;
    }

    .subheading {
      font-size: 18px;
    }

  }
</style>
