<template>
    <footer>
        <div class="content-container">
            <div class="content">
                <div class="UpperFooter  d-flex justify-content-between">
                    <div class="Contact">
                        <h6 class="text-uppercase fw-bold">Contact Info</h6>
                        <ul>
                            <li><span class="me-3"><i class="fa-solid fa-location-dot"></i></span> 2/45 Tower Street, New
                                York
                                USA</li>
                            <li><span class="me-3"><i class="fa-solid fa-phone"></i></span> Call Us On 0800 840 1010</li>
                            <li><span class="me-3"><i class="fa-solid fa-envelope"></i></span> Demo@Example.Com</li>
                        </ul>
                    </div>
                    <div class="Contact">
                        <h6 class="text-uppercase fw-bold">Information</h6>
                        <ul>
                            <li><a href="#">Product Support</a></li>
                            <li><a href="#">Checkout</a></li>
                            <li><a href="#"> Report Abuse</a></li>
                            <li><a href="#">Redeem Voucher</a></li>
                            <li><a href="#">Order Status</a></li>
                        </ul>
                    </div>
                    <div class="Contact">
                        <h6 class="text-uppercase fw-bold">useful Link</h6>
                        <ul>
                            <li><a href="#">Policies & Rules</a></li>
                            <li><a href="#">Privacy Policy</a></li>
                            <li><a href="#">License Policy</a></li>
                            <li><a href="#">My Account</a></li>
                            <li><a href="#">Locality</a></li>
                        </ul>
                    </div>
                    <div class="Contact">
                        <h6 class="text-uppercase fw-bold">NewsLetter</h6>
                        <p>Subscribe To Receive Inspiration, <br>Ideas & News In Your Inbox.</p>
                        <div>
                            <input type="email" placeholder="Enter Your Email">
                        </div>
                        <button class="btn text-uppercase">Subscribe</button>
                    </div>
                </div>
                <div class="LowerFooter ">
                    <div class="content text-center">
                        <p>© 2023 All Rights Reserved. Developed By TemplateMela</p>
                    </div>
                </div>
            </div>
        </div>
    </footer>
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

footer {
    background-color: $ColorBlack;
    font-size: 17px;
    letter-spacing: 0.6px;

    h6 {
        color: $ColorWhite;
    }

    color: lightgray;

    div.UpperFooter {
        padding-top: 110px;
        padding-bottom: 100px;
        border-bottom: 1px solid gray;

        p {
            margin-top: 3rem;
        }

        ul li {
            line-height: 40px;

            a {
                text-decoration: none;
                color: lightgray;
                transition: all .5s;
            }

            a:hover {
                color: $ColorWhite;
            }
        }

        input {
            padding: 0.54em 1.3em;
            background-color: #1c1c1c;
            border: #1c1c1c;
            color: lightgray;
            margin: 1rem 0;
        }

        button {
            background-color: $ColorWhite;
            border-radius: 0;
            padding: 12px 40px 12px 40px;
            color: $ColorBlack;
            font-weight: bold;
        }
    }

    div.LowerFooter {
        padding: 2rem 0;
    }

    p {
        margin: 0;
    }
}
</style>