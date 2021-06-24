<template>
    <div class="main">
        <h1>Hi</h1>
        <h2>Im Andres Marino</h2>
        <h3>I like Photography, Cars and Videogames</h3>
        <router-link to="/images">
            <button class="btn-pictures">
                See Pictures
            </button>
        </router-link>
        <p class="footer">
            Check out my <a href="https://portfolio-andres-marino.web.app/" target="blank" class="link">Portfolio</a>
        </p>
    </div>
</template>

<script>
export default {
    name: 'Index',   
}
</script>

<style scoped>
    .main {
        height: 100vh;
        text-align: center;
        display: flex;
        flex-direction: column;
        justify-content: center;
        align-items: center;
        background-image: url('https://steamuserimages-a.akamaihd.net/ugc/1686017249213474176/B92B9BFA9A693661E19B7B5047934C38D6D9B0E5/?imw=5000&imh=5000&ima=fit&impolicy=Letterbox&imcolor=%23000000&letterbox=false');
        background-size: cover;
        background-repeat: no-repeat;
        background-position: center;
        box-shadow: inset 0 0 0 1000px rgba(0, 0, 0, 0.425);
        color: white;
    }

    .main h1 {
        font-size: 5em;
        font-family: 'Bebas Neue', cursive;
    }

    .main h2 {
        font-size: 2.5em;
        margin-bottom: 10px;
    }

    .btn-pictures {
        background-color: rgba(255, 255, 255, 0.2);
        margin-top: 20px;
        padding: 10px 15px 10px 15px;
        font-size: 1.5em;
        font-family: 'Bebas Neue', cursive;
        border: none;
        box-shadow: 0px 0px 10px black;
        outline: none;
        border-radius: 5px;
        transition: .2s ease-out;
        cursor: pointer;
    }

    .btn-pictures:hover {
        background-color: white;
        box-shadow: 0px 0px 30px black;
    }

    .footer {
        position: absolute;
        bottom: 0;
        right: 0;
        margin: 10px;
    }

    .link {
        text-decoration: none;
        color: white;
        font-weight: bold;
        font-size: 1.3em;
    }
</style>