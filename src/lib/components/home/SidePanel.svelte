<script>
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
</script>

<style>
    .side-panel {
        flex: 1;
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .tab-buttons {
        display: flex;
        justify-content: space-between;
        border-bottom: 2px solid #f7c32d;
        margin-bottom: 10px;
    }

    .tab-buttons button {
        flex: 1;
        background: none;
        border: none;
        font-size: 16px;
        font-weight: bold;
        padding: 10px;
        cursor: pointer;
        border-bottom: 2px solid transparent;
    }

    .tab-buttons button.active {
        border-bottom: 2px solid #f7c32d;
    }

    .article-list {
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .article {
        display: flex;
        flex-direction: column;
        gap: 5px;
    }

    .details {
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 5px 20px;
        font-size: 14px;
    }

    .details h3 {
        margin: 20px;
        font-size: 15px;
        flex: 1;
    }

    .views {
        display: flex;
        align-items: center;
        font-size: 12px;
        color: gray;
        gap: 5px;
        margin-left: 20px;
    }
</style>

<div class="side-panel">
    <div class="tab-buttons">
        <button
            class:active={activeTab === 'Editor'}
            on:click={() => (activeTab = 'Editor')}
        >
            Editor's Choice
        </button>
        <button
            class:active={activeTab === 'Hot'}
            on:click={() => (activeTab = 'Hot')}
        >
            Hot Stories
        </button>
    </div>

    <div class="article-list">
        {#if activeTab === 'Editor'}
            {#each editorsChoice as article}
                <div class="article">
                    <div class="details">
                        <h3>{article.title}</h3>
                    </div>
                </div>
            {/each}
        {:else if activeTab === 'Hot'}
            {#each hotStories as article}
                <div class="article">
                    <div class="details">
                        <h3>{article.title}</h3>
                        <div class="views">
                            <span>{article.views}</span>
                            <i class="bi bi-eye"></i>
                        </div>
                    </div>
                </div>
            {/each}
        {/if}
    </div>
        
</div>
