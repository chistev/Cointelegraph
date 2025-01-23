<script>
    let language = "English";
    const changeLanguage = (newLang) => {
        language = newLang;
    };
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
    .logo {
        display: flex;
        align-items: center;
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
    .ecosystem-btn {
        border: 1px solid #fff;
        padding: 5px 10px;
        border-radius: 5px;
        display: flex;
        align-items: center;
        cursor: pointer;
    }
    .social-icons i {
        font-size: 20px;
        cursor: pointer;
    }
    .language-selector {
        display: flex;
        align-items: center;
        cursor: pointer;
    }
    .language-selector span {
        margin-left: 5px;
    }
</style>

<div class="header">
    <!-- Logo Section -->
    <div class="logo">
        <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 100 100" fill="white">
            <circle cx="50" cy="50" r="40" />
            <text x="50%" y="50%" text-anchor="middle" dy=".3em" font-size="20" fill="#000">
                CT
            </text>
        </svg>
        <span>COINTELEGRAPH</span>
    </div>

    <!-- Right Section -->
    <div class="right-section">
<div class="social-icons">
    <a href="https://twitter.com/chistev12" target="_blank" style="color: inherit;">
        <i class="bi bi-twitter"></i>
    </a>
</div>


        <!-- Language Selector -->
        <div class="language-selector" on:click={() => changeLanguage(language === "English" ? "Other" : "English")}>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" height="20">
                <circle cx="12" cy="12" r="10" />
            </svg>
            <span>{language}</span>
        </div>
    </div>
</div>
