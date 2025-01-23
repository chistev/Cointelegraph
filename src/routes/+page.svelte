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
    
    .main-content {
        display: flex;
        margin: 20px;
        gap: 20px;
    }

    .featured-article {
        flex: 2;
        position: relative;
    }

    .featured-article img {
        width: 100%;
        height: auto;
        border-radius: 10px;
    }

    .featured-article .overlay {
        position: absolute;
        top: 0;
        left: 0;
        width: 100%;
        height: 100%;
        background: rgba(0, 0, 0, 0.5);
        border-radius: 10px;
        color: white;
        display: flex;
        flex-direction: column;
        justify-content: flex-end;
        padding: 20px;
        box-sizing: border-box;
    }

    .featured-article .overlay h2 {
        margin: 0;
        font-size: 24px;
    }

    .featured-article .overlay .meta {
        font-size: 14px;
        margin-top: 10px;
    }

    .side-panel {
        flex: 1;
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .side-panel .tab-buttons {
        display: flex;
        justify-content: space-between;
        border-bottom: 2px solid #f7c32d;
        margin-bottom: 10px;
    }

    .side-panel .tab-buttons button {
        flex: 1;
        background: none;
        border: none;
        font-size: 16px;
        font-weight: bold;
        padding: 10px;
        cursor: pointer;
        border-bottom: 2px solid transparent;
    }

    .side-panel .tab-buttons button.active {
        border-bottom: 2px solid #f7c32d;
    }

    .side-panel .article-list {
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .side-panel .article-list .article {
        display: flex;
        gap: 10px;
        align-items: center;
    }

    .side-panel .article-list .article .details {
        font-size: 14px;
    }

    .side-panel .article-list .article .details h3 {
        margin: 20px;
        font-size: 15px;
        font-weight: bold;
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
    <span class="search-icon">
        <i class="bi bi-search"></i>
    </span>
</nav>

<div class="main-content">
    <!-- Featured Article -->
    <div class="featured-article">
        <img src="https://images.cointelegraph.com/cdn-cgi/image/format=auto,onerror=redirect,quality=90,width=740/https://s3.magazine.cointelegraph.com/magazine/wp-content/uploads/2025/01/magazine-Theyve-solved-cryptos-janky-UX-problem-Part-1-Inteoperabilty-scaled.jpg" alt="Placeholder Image">
        <div class="overlay">
            <h2>Ledger co-founder released after days in captivity in France: Report</h2>
            <div class="meta">
                <span>Latest News</span> | <span>by Mehab Qureshi</span> | <span>3 hours ago</span>
            </div>
        </div>
    </div>

    <!-- Side Panel -->
    <div class="side-panel">
        <div class="tab-buttons">
            <button class="active">Editor's Choice</button>
            <button>Hot Stories</button>
        </div>

        <div class="article-list">
            <div class="article">
                <div class="details">
                    <h3>Ethereum whales add $1B in ETH — Is the accumulation trend hinting at a $5K ETH price?</h3>
                </div>
            </div>
            <div class="article">
                <div class="details">
                    <h3>They solved crypto’s janky UX problem. You just haven’t noticed yet</h3>
                </div>
            </div>
            <div class="article">
                <div class="details">
                    <h3>Can the law keep up with Musk and DOGE?</h3>
                </div>
            </div>
            <div class="article">
                <div class="details">
                    <h3>House Democrats want ethics probe on Trump over crypto projects</h3>
                </div>
            </div>
            <div class="article">
                <div class="details">
                    <h3>House Democrats want ethics probe on Trump over crypto projects</h3>
                </div>
            </div>
        </div>
    </div>
</div>
