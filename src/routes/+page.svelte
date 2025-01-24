<script>
	import Logo from "$lib/components/home/Logo.svelte";
	import SidePanel from "$lib/components/home/SidePanel.svelte";
</script>

<style>
    .header {
        display: flex;
        justify-content: space-between;
        align-items: center;
        background-color: #111;
        padding: 10px 20px;
        color: #fff;
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

    .featured-article .overlay .meta span:first-child {
    color: #f7c32d;
    font-weight: bold;
}

    .navigation-arrows {
        position: absolute;
        bottom: 10px;
        right: 10px;
        display: flex;
        gap: 10px;
    }

    .navigation-arrows .arrow {
        background-color: rgba(0, 0, 0, 0.7);
        border: none;
        color: white;
        width: 35px;
        height: 35px;
        border-radius: 50%;
        display: flex;
        justify-content: center;
        align-items: center;
        cursor: pointer;
        font-size: 20px;
    }

    .navigation-arrows .arrow:hover {
        background-color: #f7c32d;
        color: black;
    }
</style>

<div class="header">
    <Logo/>

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
    <div class="featured-article">
        <img src="https://images.cointelegraph.com/cdn-cgi/image/format=auto,onerror=redirect,quality=90,width=740/https://s3.magazine.cointelegraph.com/magazine/wp-content/uploads/2025/01/magazine-Theyve-solved-cryptos-janky-UX-problem-Part-1-Inteoperabilty-scaled.jpg" alt="Placeholder Image">
        <div class="overlay">
            <h2>Ledger co-founder released after days in captivity in France: Report</h2>
            <div class="meta">
                <span>Latest News</span> | <span>by Mehab Qureshi</span> | <span>3 hours ago</span>
            </div>
        </div>

        <div class="navigation-arrows">
            <button class="arrow left"><i class="bi bi-chevron-left"></i></button>
            <button class="arrow right"><i class="bi bi-chevron-right"></i></button>
        </div>
    </div>

    <SidePanel/>
</div>
