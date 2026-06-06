<script setup>
const navLinks = [
  { id: 1, text: 'Home', url: '#' },
  { id: 2, text: 'More', url: '#' },
  { id: 3, text: 'Contact', url: '#' }
]
const plantTypes = [
  { id: 1, text: 'Indoor Plants', url: '#' },
  { id: 2, text: 'Outdoor Plants', url: '#' },
  { id: 3, text: 'Rare Species', url: '#' }
]
</script>

<template>
  <header class="site-header">
    <div class="header-logo">
      <img src="/logo-icon.png" alt="Planto Logo" class="logo-img">
      <span class="logo-text">Planto.</span>
    </div>

    <nav class="header-nav">
      <ul class="nav-list">
        <li class="nav-item"><a href="#" class="nav-link active">Home</a></li>

        <li class="nav-item dropdown">
          <span class="nav-link dropdown-toggle">
            Plant Type <span class="arrow-icon">▾</span>
          </span>
          <ul class="dropdown-menu glass-card">
            <li v-for="type in plantTypes" :key="type.id" class="dropdown-item">
              <a :href="type.url">{{ type.text }}</a>
            </li>
          </ul>
        </li>

        <li class="nav-item"><a href="#" class="nav-link">More</a></li>
        <li class="nav-item"><a href="#" class="nav-link">Contact</a></li>
      </ul>
    </nav>

    <div class="header-actions">
      <button class="action-btn" aria-label="Search">
        <img src="/search-icon.png" alt="Search icon">
      </button>
      <button class="action-btn" aria-label="Cart">
        <img src="/cart-icon.png" alt="Cart icon">
      </button>
      <button class="action-btn burger-menu" aria-label="Open menu">
        <img src="/menu-icon.png" alt="Menu icon">
      </button>
    </div>
  </header>
</template>

<style scoped>
.site-header {
  padding: 40px 60px;
  display: flex;
  align-items: center;
  justify-content: space-between;
}

.header-logo {
  cursor: pointer;
  display: flex;
  align-items: center;
  gap: 15px;
}

.logo-img {
  width: 45px;
  height: 45px;
}

.logo-text {
  font-size: 28px;
  font-weight: bold;
}

.nav-list {
  list-style: none;
  display: flex;
  gap: 60px;
  margin: 0;
  padding: 0;
}

.nav-item {
  position: relative;
}

.nav-link {
  font-size: 23px;
  color: rgba(255, 255, 255, 0.75);
  text-decoration: none;
  cursor: pointer;
  transition: color 0.3s ease;
}

.nav-link:hover,
.nav-link.active {
  color: #FFFFFF;
}

.dropdown-toggle {
  display: flex;
  align-items: center;
  gap: 5px;
}

.arrow-icon {
  font-size: 18px;
  transition: transform 0.3s ease;
}

.dropdown-menu {
  position: absolute;
  top: 100%;
  left: 50%;
  transform: translateX(-50%) translateY(10px);
  list-style: none;
  padding: 0;
  margin: 0;
  min-width: 180px;
  opacity: 0;
  visibility: hidden;
  border-radius: 12px;
  overflow: hidden;
  transition: opacity 0.3s ease, transform 0.3s ease, visibility 0.3s;
  z-index: 10;
}

.dropdown:hover .dropdown-menu {
  opacity: 1;
  visibility: visible;
  transform: translateX(-50%) translateY(0);
}

.dropdown:hover .arrow-icon {
  transform: rotate(180deg);
}

.dropdown-item a {
  display: block;
  padding: 15px 25px;
  color: #FFFFFF;
  text-decoration: none;
  font-size: 18px;
  transition: background-color 0.2s ease;
}

.dropdown-item:hover {
  background-color: rgba(255, 255, 255, 0.15);
}

.header-actions {
  display: flex;
  align-items: center;
  gap: 60px;
}

.action-btn {
  background: none;
  border: none;
  padding: 0;
  cursor: pointer;
  display: flex;
  align-items: center;
  justify-content: center;
  transition: transform 0.2s ease;
}

.action-btn:hover {
  transform: scale(1.1);
}

.action-btn img {
  width: 25px;
  height: 25px;
  object-fit: contain;
}

.burger-menu img {
  width: 30px;
  height: 10px;
}

.glass-card {
  background-color: rgba(255, 255, 255, 0.05);
  backdrop-filter: blur(25px);
  border: 1px solid rgba(255, 255, 255, 0.1);
  box-shadow: 0px 4px 15px rgba(0, 0, 0, 0.2);
}
</style>