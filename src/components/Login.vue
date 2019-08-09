<template>
    <div class="container">
        <div class="login">
            <div class="login-image"></div>
            <p>Herzlich Willkommen bei</p>
            <h2>DataGuard!</h2>
            <form v-on:submit="formSubmit($event)" action="">
                <FormInputText
                        label="Email-Adresse"
                        type="email"
                        placeholder="please enter your email-address"
                        v-bind:required="true"
                        v-model="userEmail"

                ></FormInputText>
                <FormInputText
                        type="password"
                        label="Passwort"
                        placeholder="please enter your password"
                        v-bind:required="true"
                        v-model="passWord"
                ></FormInputText>
                <div class="form-footer">
                    <FormInputButton
                            type="submit"
                            text="Anmelden"
                            colrClass="login-Btn"
                    ></FormInputButton>
                    <FormInputCheck
                            checkText="Passwort merken"
                    ></FormInputCheck>
                </div>
            </form>
            <a href="/" class="login-forget-pass">Passwort vergessen?</a>
        </div>
        <Footer></Footer>
    </div>
</template>
<script>
    import FormInputText from '../helpers/FormInputText'
    import FormInputButton from '../helpers/FormButton'
    import FormInputCheck from '../helpers/FormInputCheck'
    import Footer from '../components/Footer.vue'

    export default {
        name: 'Login',
        data() {
            return {
                userEmail:'',
                passWord:''
            }
        },
        components: {
            Footer,
            FormInputText,
            FormInputButton,
            FormInputCheck
        },
        methods:{
            formSubmit : function (e) {
                e.preventDefault();
            }
        }
    }
</script>

<style lang="scss" scoped>
    .container {
        position: absolute;
        z-index: 10;
        top: 50%;
        left: 50%;
        margin-top: -280px;
        margin-left: -430px;
        width: 860px;
        height: 660px;

    }

    .login {
        position: relative;
        width: 860px;
        height: 560px;
        box-shadow: 0px 12px 48px rgba(0, 0, 0, 0.1);
        background-color: #fff;
        padding: 128px 450px 40px 40px;

        &-image {
            position: absolute;
            background: url("../assets/guard.jpg") 810px;
            width: 325px;
            height: 100%;
            display: block;
            top: 0;
            right: 0;
            background-color: red;
        }

        p {
            font-size: 18px;
            line-height: 25px;
            margin: 0;
        }

        h2 {
            font-size: 26px;
            line-height: 35px;
            margin: 0;
        }

        &-forget-pass {
            position: absolute;
            bottom: 40px
        }
    }

    .form-footer {
        margin-top: 35px;
        display: flex;

        .form-element-input-button {
            flex: 2;
        }

        .form-element-input-check {
            padding-top: 10px;
            flex: 1;
        }
    }

    @media only screen and (max-width: 768px) {
        .container {
            width: 375px;
            left: 0;
            right: 0;
            margin-left: auto;
            margin-right: auto;
            margin-top: 0;
            top: 0;
        }
        .login {
            width: 375px;
            left: 0;
            right: 0;
            margin-left: auto;
            margin-right: auto;
            padding: 160px 20px 20px 20px;

            &-image {
                width: 100%;
                height: 140px;
                background: url(/img/guard.743bf2ce.jpg);
                background-size: 280%;
                background-position-x: 598px;
                background-position-y: 468px;
            }

            &-forget-pass {
                bottom: 20px
            }
        }

        .form-footer {
            .form-element-input-check {
                flex: 1.1; //todo : Refine this quick fix
            }
        }

    }

</style>