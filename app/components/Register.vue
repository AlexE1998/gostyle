<template>
    <Page class="page">
        <ActionBar title="Connexion" flat="true" />
        <BottomNavigation>
            <TabContentItem>
                <GridLayout
                    rows="auto,auto,auto,auto,auto,auto,auto,auto,auto,auto,auto,auto,auto,auto,auto">
                    <Label row="1" class="loginForm resizeTop "
                        text="Nom :" />
                    <TextField row="2" class="loginForm resizeBottom"
                        v-model="nameRegisterValue" hint="Ex : Dupont " />

                    <Label row="3" class="loginForm" text="Prénom :" />
                    <TextField row="4" class="loginForm resizeBottom"
                        v-model="usernameRegisterValue" hint="Ex : Alain" />

                    <Label row="5" class="loginForm" text="E-mail :" />
                    <TextField row="6" class="loginForm resizeBottom"
                        v-model="emailRegisterValue"
                        hint="Ex : mail@mail.com" />

                    <Label row="7" class="loginForm" text="Pseudo :" />
                    <TextField row="8" class="loginForm resizeBottom"
                        v-model="pseudoRegisterValue" hint="Ex : Dupont44" />

                    <Label row="9" class="loginForm" text="Mot de passe :" />
                    <TextField row="10" secure="true"
                        class="loginForm resizeBottom"
                        v-model="usernameRegisterValue" hint="Ex : 123AbCd" />

                    <Button row="11" class="buttonLogin" text="Valider"
                        @tap="onCreateAccount" />

                </GridLayout>
            </TabContentItem>
        </BottomNavigation>

    </Page>
</template>

<script>
    export default {
        data() {
            return {};
        }
    };
</script>

<style>
</style>