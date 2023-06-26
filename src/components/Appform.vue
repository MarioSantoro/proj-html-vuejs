<template >
    <div class="content-container margin-bottom-cs margin-top-cs">
        <h6 class="fw-bold">COLLABORATE</h6>
        <div class="content-form d-flex">
            <div class="text ">
                <h2 class="mb-4 fw-bold">WANT TO WORK WITH US? <br> LEAVE US A MESSAGE!</h2>
                <p>
                    Duis sit amet congue ipsum. Nulla maximus My venenatis posuere.To The Mauris ut tempus Suspendisse porta
                    tincidunt lectus non of me pellentesque. At A Sed blandit at diam sit amet Orci varius natoque penatibus
                    et
                    dis dis to parturient montes, My Car nascetur ridiculus Sed feugiat lacus in erat egestas, quis eleifend
                    lacus imperdiet.
                </p>
            </div>
            <div class="form">
                <div class="row-input d-flex justify-content-between">
                    <input type="text" placeholder="Your Name">
                    <input type="email" placeholder="Your email">
                </div>
                <div class="row-input d-flex justify-content-between mb-4">
                    <input type="text" placeholder="Your number">
                    <input type="text" placeholder="Your Pincode">
                </div>
                <div class="row-text-area">
                    <textarea class="area" cols="43" rows="6" placeholder="Enter your Message"></textarea>
                </div>
                <button class="btn">Sumbit Now</button>
            </div>
        </div>
    </div>
</template>
<script>
export default {
    data() {
        return {

        }
    }
}
</script>
<style lang="scss" scoped>
@use '../styles/utilities/variables.scss' as *;

div.text {
    width: 50%;
    padding-right: 2rem;

    h2 {
        font-size: 40px;
    }

    p {
        letter-spacing: 0.6px;
    }
}

div.form {
    width: 50%;

    div.row-input input {
        width: calc(100% / 2 - 20px);
        margin-bottom: 1.5rem;
        background: $ColorLightGray;
        border: none;
        padding: 0.54em 1.3em
    }

    div.row-text-area .area {
        width: 100%;
        background: $ColorLightGray;
        border: none;
        padding: 0.54em 1.3em
    }

    button {
        background-color: $ColorBlack;
        width: 100%;
        color: $ColorWhite;
        text-transform: uppercase;
        font-weight: bold;
        border-radius: 0;
        margin-top: 2rem;
        padding: 12px 40px 12px 40px
    }
}

p {
    color: $ColorGray;
}
</style>