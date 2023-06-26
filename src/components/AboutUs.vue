<template>
    <div class="container-about d-flex ">
        <div class="content-about d-flex align-items-center">
            <div class="content ">
                <p class="text-uppercase fw-bold">About Us</p>
                <h1 class="text-uppercase fw-bold my-4">HIGH QUALITY CINEMATICS</h1>
                <p class="text fw-bold">Orci varius penatibus et magnis dis parturient In the montes, nascetur ridiculus
                    mus. Nulla
                    A nisi ut mi efficitur hendrerit. nunc urna. quisque a partr hendrerit purus erat, nec dapibus
                    sem sed. phasellus sed eli molestie, porttitor ligula of the egestas, mattis augue. quisque et
                    rhoncus justo. suspendisse luctus pharetra eleme tcondimentum.</p>
                <button class="btn btn-light text-uppercase fw-semibold">Read more</button>
            </div>
        </div>
    </div>
    <h1>Droga</h1>
</template>
<script>
export default {

}
</script>
<style lang="scss" scoped>
@use "../styles/utilities/variables.scss" as *;

div.container-about {
    background-color: #0a1010;
    height: 575px;
    background-image: url(../assets/About-Us.jpg);
    background-repeat: no-repeat;
    background-position: end;


    div.content-about {
        height: 575px;
        width: 50%;
        position: absolute;
        right: 0;
        color: $ColorWhite;

        p.text {
            width: 700px;
            line-height: 30px;
        }

        button {
            border-radius: 0;
            font-size: 15px;
            padding: 9px 30px;
        }
    }
}
</style>