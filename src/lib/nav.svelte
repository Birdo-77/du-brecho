<script></script>

<main>
    <nav>
        <div class="home">
            <div class="logo"></div>
        </div>
        <h1>Du brecho</h1>
    <div class="account">
        <span class="material-symbols-sharp">
            account_circle
        </span>
        <span class="material-symbols-sharp">
            shopping_cart
        </span>
        <span class="material-symbols-sharp">
            info
        </span>
    </div>
    </nav>
</main>

<style>
    nav{
        color: #b98c4c;
        background-color: #000000;
        width: 100%;
        padding: 0 10px;
        display: flex;
        align-items: center;
        justify-content: space-between;
        border-bottom: 2px dotted black;
    }
    .logo{
        height: 60px;
        width: 60px;
        background-image: url("logo.png");
        background-position: center;
        background-size: contain;
        background-repeat: no-repeat;
    }
    .home{
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .search{
        border: 2px solid #3c4400;
        height: 100%;
        width: 40%;
        display: flex;
        padding: 2px 0px;
        align-items: center;
    }
    .account{
        margin-right: 5px;
    }
    .account span{
        margin-right: 7px;
    }
    input{
        background-color: black;
        border: 0;
        outline: none;
        box-shadow: none;
        width: 60%;
        flex: 1;
        font-size: 1rem;
    }
    .search-icon{
        color: white;
        padding: 0px 10px;
        text-align: center;
    }
</style>