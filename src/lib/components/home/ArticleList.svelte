<script lang="ts">
    export let activeTab: string;
    export let editorIndex: number;
    export let hotIndex: number;
    export let editorsChoice: { title: string }[];
    export let hotStories: { title: string, views: number }[];
  </script>
  
  <div class="article-list">
    {#if activeTab === 'Editor'}
      {#each editorsChoice as article, index}
        <div class="article {index === editorIndex ? 'first-article' : ''}">
          <div class="details">
            <h3>{article.title}</h3>
          </div>
        </div>
      {/each}
    {:else if activeTab === 'Hot'}
      {#each hotStories as article, index}
        <div class="article {index === hotIndex ? 'first-article' : ''}">
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
  
  <style>
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
  
    .first-article h3 {
      font-weight: bold;
    }
  </style>
  