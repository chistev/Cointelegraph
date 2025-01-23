<style>
    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: #111;
        padding: 10px 20px;
        color: #fff;
    }

    .logo {
        display: flex;
        align-items: center;
        color:#f7c32d
    }

    .logo svg {
        height: 40px;
        margin-right: 10px;
    }

    .right-section {
        display: flex;
        align-items: center;
        gap: 20px;
    }

    .social-icons i {
        font-size: 20px;
        cursor: pointer;
    }

    .navbar {
        display: flex;
        justify-content: center;
        align-items: center;
        background-color: #f7c32d;
        padding: 10px;
    }

    .navbar a {
        color: black;
        text-decoration: none;
        margin: 0 15px;
        font-size: 16px;
        font-weight: bold;
    }

    .navbar a:hover {
        text-decoration: underline;
    }

    .navbar .search-icon {
        margin-left: auto;
        font-size: 20px;
        cursor: pointer;
    }
</style>

<div class="header">
    <div class="logo">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" fill="white">
            <circle cx="50" cy="50" r="40" />
            <text x="50%" y="50%" text-anchor="middle" dy=".3em" font-size="20" fill="#000">
                CT
            </text>
        </svg>
        <span>COINTELEGRAPH</span>
    </div>

    <div class="right-section">
        <div class="social-icons">
            <a href="https://twitter.com/chistev12" target="_blank" style="color: inherit;">
                <i class="bi bi-twitter"></i>
            </a>
        </div>
    </div>
</div>

<nav class="navbar">
    <a href="#news">News</a>
    <a href="#indices">Indices</a>
    <a href="#in-depth">In Depth</a>
    <a href="#learn">Learn</a>
    <a href="#crypto-bonus">Crypto Bonus</a>
    <a href="#research">Research</a>
    <a href="#podcasts">Podcasts</a>
    <a href="#about">About</a>
    <span class="search-icon">🔍</span>
</nav>
