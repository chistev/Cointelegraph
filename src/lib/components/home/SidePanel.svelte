  <style>
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
  