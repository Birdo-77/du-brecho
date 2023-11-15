<script>
    const clothes = [
        {
            name: "Camisa Florida Branco/Preto",
            price: 12.00,
        },
        {
            name: "Camiseta Super Mario",
            price: 6.00,
        },
        {
            name: "Camisa Preta Estampa Tigre",
            price: 11.00,
        },
        {
            name: "Camisa Preta Training",
            price: 12.00,
        },
        {
            name: "Camiseta Stella Artois",
            price: 12.00,
        },
        {
            name: "Camiseta Black Sabbath",
            price: 13.00,
        },
        {
            name: "Camiseta Simpsons",
            price: 14.00,
        },
        {
            name: "Camiseta Vermelha",
            price: 12.00,
        },
        {
            name: "Camiseta Branca Gato",
            price: 14.00,
        },
        {
            name: "Camiseta Itachi",
            price: 15.00,
        },
        {
            name: "Blusa Cobra D'agua",
            price: 22.00,
        },
    ];

    const changeView = (el) => {
        const back = document.getElementById("b-" + el.target.id);
        back.classList.remove("hide");
        el.target.classList.add("hide");
        back.animate([
            {opacity: "80%",
            filter: "brightness(30%)"},
            {opacity: "100%",
            filter: "brightness(100%)"},
        ], {duration: 1000, 
            iterations: 1,}
        )
    }

    const frontView = (el) => {
        const front = document.getElementById(el.target.id.toString().replace("b-", ""));
        front.classList.remove("hide");
        el.target.classList.add("hide");
        front.animate([
            {opacity: "80%",
            filter: "brightness(10%)"},
            {opacity: "100%",
            filter: "brightness(100%)"},
        ], {duration: 2000, 
            iterations: 1,}
        )
    }
</script>

<main>
    <h1>Roupas Disponíveis</h1>
    <h3>Tempo limitado</h3>

    <section>
        {#each clothes as cl, index}
            <div class="cl">
                <img src='../src/assets/clothes/{index + 1}-front.jpg' alt="" id="{index.toString()}" on:mouseenter={changeView}>
                <img src='../src/assets/clothes/{index + 1}-back.jpg' class="hide" id="b-{index}" alt="" on:mouseleave={frontView}>
                <h1>{cl.name}</h1>
                <div class="price">
                    <p>Por: R${cl.price},00</p>
                    <a href="#footer">Comprar</a>
                </div>
            </div>
        {/each}
    </section>
</main>

<style>
    main{
        padding-top: 60px;
        width: 85%;
        margin: 0 auto;
    }
    
    h3{
        font-weight: lighter;
    }

    section{
        margin-top: 50px;
        width: 100%;
        display: flex;
        align-items: center;
        justify-content: space-around;
        flex-wrap: wrap;
        gap: 2rem;
    }

    .cl{
        display: flex;
        flex-direction: column;
        width: 33,33%;
    }

    .cl img{
        align-self: center;
        width: 280px;
        height: auto;
        object-fit: cover;
    }

    .cl h1{
        text-align: center;
        font-size: 1.3rem;
        font-weight: normal;
    }

    .cl .price{
        display: flex;
        justify-content: space-evenly;
    }

    .hide{
        position: absolute;
        left: -999px;
    }

    a{
        text-decoration: none;
        border-bottom: 1px solid black;
    }
</style>