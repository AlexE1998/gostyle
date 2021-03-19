<template>
    <Page class="page">
        <ActionBar title="Connexion" flat="true" />
        <BottomNavigation>
            <TabContentItem>
                <GridLayout rows="auto,auto,auto,auto,auto,auto,auto">
                    <Label row="1" class="loginForm resizeTop "
                        text="Pseudo :" />
                    <TextField row="2" class="loginForm resizeBottom"
                        v-model="usernameLoginValue" hint="Ex : Dupont44 " />
                    <Label row="3" class="loginForm" text="Mot de passe :" />
                    <TextField row="4" secure="true"
                        class="loginForm resizeBottom"
                        v-model="passwordLoginValue" hint="Ex : 123AbCd" />
                    <Button row="5" class="buttonLogin" text="Connexion"
                        @tap="onLoginTap" />
                    <Button row="6" class="buttonLogin" text="Nouveau compte"
                        @tap="onRegisterTap" />
                </GridLayout>
            </TabContentItem>
        </BottomNavigation>

    </Page>
</template>

<script>
    import Register from "./Register";
    export default {
        methods: {
            onButtonTap() {
                console.log("Button was pressed");
            },

            onItemTap: function(args) {
                console.log("Item with index: " + args.index + " tapped");
            },
            onRegisterTap() {
                this.$navigateTo(Register);
            }
        }
    };
</script>

<style scoped>
    .loginForm {
        font-size: 16;
        margin-left: 50;
        margin-right: 50;
    }

    .resizeTop {
        margin-top: 50;
    }

    .resizeBottom {
        margin-bottom: 50;
    }

    .buttonLogin {
        background-color: #43378E;
    }
</style>