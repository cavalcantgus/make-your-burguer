<template>
    <v-dialog v-model="localVisible" width="500px">
        <v-card class="custom-card">
            <v-card-title>
                <span class="card-title">Make your burguer</span>
                <v-form ref="form">
                    <v-text-field type="text"
                    label="Nome do cliente" class="input-field"></v-text-field>
                    <v-combobox label="Escolha o pão" class="input-field"></v-combobox>
                    <v-combobox label="Escolha a carne do seu Burguer" class="input-field"></v-combobox>
                    <v-span class="opcionais">Selecione os opcionais</v-span>
                    <v-checkbox label="Salame" class="input-field"></v-checkbox>
                    <v-card-actions>
                        <v-btn class="cancel-button" @click="close">Cancelar</v-btn>
                        <v-btn class="save-button" @click="save">Fazer pedido</v-btn>
                    </v-card-actions>
                </v-form>
            </v-card-title>
        </v-card>
    </v-dialog>
</template>

<script>
export default {
    name: 'BurguerForm',
    props: {
        visible: Boolean
    },
    data() {
        return {
            localVisible: this.visible
        }
    },
    watch: {
        visible(newValue) {
            this.localVisible = newValue
        }
    },
    methods: {
        close() {
            this.$emit('cancel')
        },
        save() {
            this.$emit('save')
        }
    }
}
</script>

<style scoped>
    .custom-card {
        border-radius: 20px;
        background-color: rgb(218, 217, 217);
    }

    .card-title {
        text-align: center;
        color: rgb(211, 169, 30);
        width: 100%;
        display: block;
        margin-bottom: 16px;
        font-size: 20px;
        font-weight: bold;
    }

    .input-field {
        color: rgb(26, 26, 26);
    }
    
    .opcionais {
        color: rgb(211, 169, 30);
    }

    .save-button {
        background-color: #222;
        color: rgb(211, 169, 30);
        font-weight: bold;
        border: 2px solid #222;
        padding: 10px;
        font-size: 16px;
        cursor: pointer;
    }

    .cancel-button {
        background-color: #222;
        color: rgb(211, 169, 30);
         font-weight: bold;
        border: 2px solid #222;
        padding: 10px;
        font-size: 16px;
        cursor: pointer;
    }
</style>