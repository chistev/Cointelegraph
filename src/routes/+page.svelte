<script lang="ts">
    let language = "English";
    let showDropdown = false;

    // Function to change language
    const changeLanguage = (newLang: string) => {
        language = newLang;
    };

    // Function to toggle dropdown visibility
    const toggleDropdown = () => {
        showDropdown = !showDropdown;
    };

    // Close the dropdown when clicked outside
    const handleClickOutside = (event: MouseEvent) => {
        const dropdown = document.getElementById("language-dropdown");
        if (dropdown && !dropdown.contains(event.target as Node)) {
            showDropdown = false;
        }
    };

    // Attach the click outside listener when the component is mounted
    import { onMount, onDestroy } from "svelte";
    onMount(() => {
        document.addEventListener("click", handleClickOutside);
    });

    onDestroy(() => {
        document.removeEventListener("click", handleClickOutside);
    });
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

    .social-icons i {
        font-size: 20px;
        cursor: pointer;
    }

    .language-selector {
        display: flex;
        align-items: center;
        cursor: pointer;
        position: relative; /* Necessary for positioning the dropdown */
    }

    .language-selector span {
        margin-left: 5px;
    }

    .dropdown-menu {
        position: absolute;
        top: 30px; /* Adjust this based on your design */
        left: 0;
        background-color: #333;
        padding: 10px;
        border-radius: 5px;
        width: 120px;
        box-shadow: 0 4px 8px rgba(0, 0, 0, 0.2);
        display: block;
        visibility: visible;
        opacity: 1;
        transition: opacity 0.3s ease, visibility 0.3s ease;
    }

    .dropdown-menu.hidden {
        visibility: hidden;
        opacity: 0;
    }

    .dropdown-menu a {
        display: block;
        padding: 5px;
        color: #fff;
        text-decoration: none;
    }

    .dropdown-menu a:hover {
        background-color: #444;
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
        <div class="language-selector" on:click={toggleDropdown}>
            <svg xmlns="http://www.w3.org/2000/svg" viewBox="0 0 24 24" fill="white" height="20">
                <circle cx="12" cy="12" r="10" />
            </svg>
            <span>{language}</span>

            <!-- Dropdown Menu -->
            <div id="language-dropdown" class="dropdown-menu {showDropdown ? '' : 'hidden'}">
                <a href="#" on:click={() => changeLanguage('English')}>English</a>
                <a href="#" on:click={() => changeLanguage('Other')}>Other</a>
            </div>
        </div>
    </div>
</div>
