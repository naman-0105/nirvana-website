<script>
  import { createEventDispatcher } from 'svelte';
  const dispatch = createEventDispatcher();
  let menuOpen = false;

  const toggleMenu = () => {
    menuOpen = !menuOpen;
  };

  const handleMenuClick = (page) => {
    menuOpen = false;
    dispatch('changePage', page);
  };
</script>

<style>
  @import url('https://fonts.googleapis.com/css2?family=Kreon:wght@300;400;500;700&display=swap');
  nav {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 10px 30px;
    background-color: #f4f4f4;
    color: #000;
    position: relative;
    box-sizing: border-box;
    width: 100%;
  }

  .logo {
    display: flex;
    align-items: center;
    gap: 10px;
  }

  .logo img {
    width: 50px;
    height: 50px;
  }

  .logo-font {
    font-family: 'Kreon', serif;
    font-size: 1.5rem;
    font-weight: bold;
  }

  ul {
    list-style-type: none;
    display: flex;
    gap: 80px;
    margin-right: 20px;
    padding: 0;
  }

  ul li {
    font-size: 16px;
    font-weight: 550;
    cursor: pointer;
  }

  ul li:hover {
    color: #FF6F00;
  }

  .hamburger {
  display: none;
  flex-direction: column;
  justify-content: space-between;
  cursor: pointer;
  width: 30px;
  height: 25px;
  position: relative;
  z-index: 2;
}

.hamburger div {
  width: 100%;
  height: 3px;
  background-color: #000;
  transition: all 0.3s ease-in-out;
}

.hamburger.open div:nth-child(1) {
  transform: rotate(45deg) translate(5px, 5px);
  background-color: #000;
}

.hamburger.open div:nth-child(2) {
  opacity: 0;
}

.hamburger.open div:nth-child(3) {
  transform: rotate(-45deg) translate(5px, -5px);
  background-color: #000;
}

  .menu-dropdown {
    position: absolute;
    top: 100%;
    left: 0;
    width: 100%;
    background: white;
    color: black;
    padding: 20px;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    gap: 15px;
    box-shadow: 0 4px 6px rgba(53, 52, 52, 0.2);
    transform: translateY(-20px);
    opacity: 0;
    visibility: hidden;
    transition: all 0.3s ease-in-out;
    z-index: 10;
    box-sizing: border-box;
  }

  .menu-dropdown.open {
    transform: translateY(0);
    opacity: 1;
    visibility: visible;
    z-index: 10;
  }

  .menu-dropdown a {
    text-decoration: none;
    color: black;
    font-size: 1.2rem;
    text-align: center;
    transition: background-color 0.3s ease-in-out;
    padding: 10px;
    border-radius: 5px;
    display: block;
  }

  .menu-dropdown a:hover {
    background: rgba(255, 255, 255, 0.2);
    cursor: pointer;
  }

  .menu-dropdown a + a {
    border-top: 1px solid black;
  }

  @media screen and (max-width: 768px) {
    ul {
      display: none;
    }

    .hamburger {
      display: flex;
    }

    .menu-dropdown {
      display: flex;
    }
  }
</style>

<nav>
  <div class="logo">
    <img src="/NirvanaLogo.png" alt="Nirvana Logo" />
    <h1 class="logo-font">NIRVANA</h1>
  </div>

  <!-- Hamburger Menu -->
  <div class="hamburger {menuOpen ? 'open' : ''}" on:click={toggleMenu}>
    <div></div>
    <div></div>
    <div></div>
  </div>

  <!-- Dropdown Menu -->
  <div class="menu-dropdown {menuOpen ? 'open' : ''}">
    <a on:click={() => handleMenuClick('home')}>HOME</a>
    <a on:click={() => handleMenuClick('about')}>ABOUT</a>
    <a on:click={() => handleMenuClick('events')}>EVENTS</a>
    <a on:click={() => handleMenuClick('team')}>TEAM</a>
  </div>

  <!-- Desktop Navigation Menu -->
  <ul>
    <li on:click={() => handleMenuClick('home')}>HOME</li>
    <li on:click={() => handleMenuClick('about')}>ABOUT</li>
    <li on:click={() => handleMenuClick('events')}>EVENTS</li>
    <li on:click={() => handleMenuClick('team')}>TEAM</li>
  </ul>
</nav>
