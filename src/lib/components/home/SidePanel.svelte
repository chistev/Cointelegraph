<script lang="ts">
	import { onMount } from "svelte";
    import ArticleList from "./ArticleList.svelte";

    export let activeTab = 'Editor';
    export let editorIndex = 0;
    export let hotIndex = 0;
    
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

    let intervalId: number;

    const changeArticle = () => {
    if (activeTab === 'Editor') {
      editorIndex = (editorIndex + 1) % editorsChoice.length;
      if (editorIndex === 0) {
        activeTab = 'Hot';
      }
    } else if (activeTab === 'Hot') {
      hotIndex = (hotIndex + 1) % hotStories.length;
      if (hotIndex === 0) {
        activeTab = 'Editor';
      }
    }
  };

  onMount(() => {
    intervalId = setInterval(changeArticle, 10000);

    return () => clearInterval(intervalId);
  });
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

    <ArticleList 
    {activeTab} 
    {editorIndex} 
    {hotIndex} 
    {editorsChoice} 
    {hotStories} 
  />
</div>