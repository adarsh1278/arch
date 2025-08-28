<script>
    export let heading = "Spaces that tell your story";
    export let description =
        "Every corner whispers memories, every room holds dreams waiting to unfold";
    export let imageSrc = "/aboutus2.png";
</script>

<div class="container scroll-card-2">
    <div class="box-wrapper">
        <div class="circle"></div>
        <div class="rect"></div>
        <img class="image" src={imageSrc} alt="" />
    </div>

    <p class="heading">{heading}</p>

    <p class="para">{description}</p>
</div>

<style>
    .container {
        position: relative;
        width: 100vw;
        height: 100vh;
        background: #efe8db;
        margin: 0;
        padding: 0;
        box-sizing: border-box;
    }

    .box-wrapper {
        position: absolute;
        width: 503px;
        height: 655px;
        top: 48px;
        left: 484px;
    }

    .circle {
        position: absolute;
        width: 110px;
        height: 110px;
        top: 545px;
        left: 393px;
        background: #8b3a3a;
        border-radius: 55px;
    }

    .rect {
        position: absolute;
        width: 295px;
        height: 452px;
        top: 0;
        left: 0;
        background: #8b3a3a;
    }

    .image {
        position: absolute;
        width: 424px;
        height: 576px;
        top: 24px;
        left: 24px;
        object-fit: cover;
    }

    .heading {
        position: absolute;
        width: 380px;
        top: 71px;
        left: 64px;
        font-family: "Playfair Display", Helvetica, serif;
        font-weight: 400;
        font-size: 3rem;
        line-height: 56px;
        letter-spacing: -0.48px;
        color: #8b3a3a;
    }

    .para {
        position: absolute;
        width: 321px;
        top: 213px;
        left: 64px;
        font-family: "Instrument Sans", sans-serif;
        font-size: 20px;
        font-weight: 400;
        line-height: 28px;
        letter-spacing: 0.2px;
        font-style: normal;
        color: #171717;
    }

    @media (max-width: 768px) {
        .box-wrapper {
            width: 90%;
            height: auto;
            left: 5%;
            top: 10%;
        }

        .heading {
            width: 90%;
            left: 5%;
            font-size: 2rem;
            line-height: 2.5rem;
        }

        .para {
            width: 90%;
            left: 5%;
            top: 40%;
            font-size: 18px;
            line-height: 24px;
        }

        .image {
            width: 90%;
            height: auto;
            left: 5%;
            top: 5%;
        }

        .circle {
            width: 60px;
            height: 60px;
            top: auto;
            bottom: 10%;
            right: 10%;
        }

        .rect {
            width: 80%;
            height: 60%;
            left: 10%;
            top: 20%;
        }
    }
</style>
