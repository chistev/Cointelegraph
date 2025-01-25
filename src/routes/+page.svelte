<script>
    import FeaturedArticle from "$lib/components/home/FeaturedArticle.svelte";
	import Logo from "$lib/components/home/Logo.svelte";
    import SidePanel from "$lib/components/home/SidePanel.svelte";

    let editorIndex = 0; // Track the bold article in the 'Editor' tab
    let hotIndex = 0; // Track the bold article in the 'Hot' tab
    let activeTab = 'Editor';

    const hotStories = [
        { title: "Bitcoin drops after Trump signs crypto and ‘national digital asset stockpile’ executive order", views: 32951 },
        { title: "WazirX gets Singapore court approval to repay victims of $235M hack", views: 19008 },
        { title: "Upbit, Bithumb compensate users after service outages during martial law", views: 18884 },
        { title: "‘Bitcoin reserve or nothing’ — Ripple slammed for pushing multi-asset reserve", views: 18669 },
        { title: "SEC cancels controversial crypto accounting rule SAB 121", views: 18365 },
    ];

    const editorsChoice = [
        { title: "Ethereum whales add $1B in ETH — Is the accumulation trend hinting at a $5K ETH price?" },
        { title: "They solved crypto’s janky UX problem. You just haven’t noticed yet" },
        { title: "Can the law keep up with Musk and DOGE?" },
        { title: "House Democrats want ethics probe on Trump over crypto projects" },
        { title: "House Democrats want ethics probe on Trump over crypto projects" },
    ];

    // The goRight and goLeft functions that handle the navigation
    function goRight() {
        if (activeTab === 'Editor') {
            editorIndex++;
            if (editorIndex >= editorsChoice.length) {
                activeTab = 'Hot';  // Switch to Hot stories when reaching the end
                editorIndex = 0;    // Start from the first article in the new tab
            }
        } else {
            hotIndex++;
            if (hotIndex >= hotStories.length) {
                activeTab = 'Editor'; // Switch to Editor's choice when reaching the end
                hotIndex = 0;         // Start from the first article in the new tab
            }
        }
    }

    function goLeft() {
        if (activeTab === 'Editor') {
            editorIndex--;
            if (editorIndex < 0) {
                activeTab = 'Hot';  // Switch to Hot stories when reaching the start
                editorIndex = editorsChoice.length - 1;  // Start from the last article in the new tab
            }
        } else {
            hotIndex--;
            if (hotIndex < 0) {
                activeTab = 'Editor'; // Switch to Editor's choice when reaching the start
                hotIndex = hotStories.length - 1; // Start from the last article in the new tab
            }
        }
    }
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
        <FeaturedArticle
    title="Ledger co-founder released after days in captivity in France: Report"
    author="Mehab Qureshi"
    timeAgo="3 hours ago"
    imageUrl="https://images.cointelegraph.com/cdn-cgi/image/format=auto,onerror=redirect,quality=90,width=740/https://s3.magazine.cointelegraph.com/magazine/wp-content/uploads/2025/01/magazine-Theyve-solved-cryptos-janky-UX-problem-Part-1-Inteoperabilty-scaled.jpg" 
    onGoLeft={goLeft}    
        onGoRight={goRight}
  />

  <SidePanel {activeTab} {editorIndex} {hotIndex} />
</div>
