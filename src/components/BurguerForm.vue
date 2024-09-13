<template>
    <v-dialog>
        <v-card>
            <v-card-title>
                <span>Make your burguer</span>
                <v-form ref="form">
                    <v-text-field type="text"
                    label="Nome do cliente"></v-text-field>
                    <v-combobox label="Escolha o pão"></v-combobox>
                    <v-combobox label="Escolha a carne do seu Burguer"></v-combobox>
                </v-form>
            </v-card-title>
        </v-card>
    </v-dialog>
</template>