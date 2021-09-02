<script></script>

<hr />
<div class="page-section half-page-section">
    <div class="centered-container">
        <div class="section-content">
            <div class="img-container">
                <img src="assets/icon-pin.svg" alt="pin" />
            </div>
            <span class="accent">Sustainability</span>
            <div class="text-container">
                How much can &nbsp;<span class="accent">your country</span
                >&nbsp; save with refour?
            </div>

            <div class="cta-container">
                <div class="cta-button">Read more</div>
            </div>
        </div>
        <div class="section-content">
            <div class="img-container">
                <img src="assets/icon-company.svg" alt="pin" />
            </div>
            <span class="accent">Material</span>
            <div class="text-container">
                How much can &nbsp;<span class="accent">your company</span
                >&nbsp; save with refour?
            </div>

            <div class="cta-container">
                <div class="cta-button">Read more</div>
            </div>
        </div>
    </div>
</div>
<hr />
<div class="page-section half-page-section">
    <div class="single-section-container">
        <div class="text-container">DO YOU HAVE ANY QUESTIONS?</div>
        <span
            >Lorem ipsum dolor sit amet, consetetur sadipscing elitr, sed diam
            nonumy</span
        >

        <div class="cta-container">
            <div class="cta-button">Contact us</div>
        </div>
    </div>
</div>

<style>
    .cta-button {
        background-color: var(--accent-color);
        width: 180px;
        height: 60px;
        border-radius: 7px;
        color: white;

        font-weight: bold;
        text-transform: uppercase;

        align-items: center;
        justify-content: center;

        transition: 0.3s;

        cursor: pointer;
    }
    .cta-button:hover {
        width: 150px;
        height: 50px;
        background-color: #f26b3c;
    }
    .cta-container {
        width: 180px;
        height: 50px;
        transition: 0.3s;
        align-items: center;
        justify-content: center;
        border-radius: 7px;
        border: 0.5px solid var(--accent-color);
        margin-top: 10px;
    }
    .cta-container:hover {
        border: 1.5px dashed var(--accent-color);
        width: 180px;
        height: 60px;
        margin-top: 0;
    }
    .section-content {
        flex-direction: column;
        width: 50%;
        align-items: center;
        justify-content: flex-start;
    }
    .section-content:nth-child(1) {
        border-right: 2px dashed #4040411a;
    }
    .single-section-container {
        flex-direction: column;
        width: 100%;
        align-items: center;
    }
    .single-section-container > span {
        margin: 20px 0px;
    }
    hr {
        border: 2px dashed #4040411a;
        border-style: none none dashed;
        color: var(--bg-color);
        background-color: var(--bg-color);
    }
    img {
        height: 45px;
    }
    .img-container {
        height: 100px;
        width: 100px;

        align-items: center;
        justify-content: center;

        border-radius: 50%;
        border: 1.5px dashed var(--accent-color);
        margin-bottom: 20px;
    }

    .text-container {
        margin: 20px 0px 10px 0;
        width: 60%;
        font-size: 30px;
        font-weight: bold;
        display: initial;
        text-align: center;
    }
    .accent {
        display: initial;
    }
    @media only screen and (max-width: 1110px) {
        hr {
            margin-top: 10px;
        }
        .centered-container {
            flex-direction: column;
            width: 100%;
            height: 100%;
        }
        img {
            height: 30px;
        }
        .img-container {
            height: 75px;
            width: 75px;
        }
        .section-content {
            height: 50%;
            width: 100%;
        }
        .section-content:nth-child(1) {
            border-right: none;
        }
        .text-container {
            width: 100%;
        }
        .img-container {
            margin-top: 30px;
        }
        .cta-container {
            width: 140px;
            height: 40px;
        }
        .cta-container:hover {
            width: 140px;
            height: 45px;
        }
        .cta-button {
            width: 140px;
            height: 45px;
        }
        .cta-button:hover {
            height: 40px;
            width: 140px;
        }
        .text-container {
            font-size: 24px;
            margin-top: 10px;
        }
    }
</style>
