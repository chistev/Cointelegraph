<script>
    export let title = "Ledger co-founder released after days in captivity in France: Report";
    export let author = "Mehab Qureshi";
    export let timeAgo = "3 hours ago";
    export let imageUrl = "https://images.cointelegraph.com/cdn-cgi/image/format=auto,onerror=redirect,quality=90,width=740/https://s3.magazine.cointelegraph.com/magazine/wp-content/uploads/2025/01/magazine-Theyve-solved-cryptos-janky-UX-problem-Part-1-Inteoperabilty-scaled.jpg"; 
  </script>
  
  <style>
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
  
  <div class="featured-article">
    <img src={imageUrl} alt="Placeholder Image">
    <div class="overlay">
      <h2>{title}</h2>
      <div class="meta">
        <span>Latest News</span> | <span>by {author}</span> | <span>{timeAgo}</span>
      </div>
    </div>
  
    <div class="navigation-arrows">
      <button class="arrow left"><i class="bi bi-chevron-left"></i></button>
      <button class="arrow right"><i class="bi bi-chevron-right"></i></button>
    </div>
  </div>
  