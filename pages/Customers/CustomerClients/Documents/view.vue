<template>
  <card-default :clientInfo="clientInfo">
    <div class="options">
      <v-btn class="btnEdit" size="small" elevation="2" variant="text">
        Editar documentos
      </v-btn>
    </div>
    <div v-for="(document, index) in documents" :key="index">
      <document-view :document="document" />
    </div>
  </card-default>
</template>

<script>
import DocumentView from "~~/components/DocumentView.vue";
import CardDefault from "~~/components/CardDefault.vue";

export default {
  data() {
    return {
      documents: [
        {
          name: "Cadastro Nacional da Pessoa Jurídica - CNPJ ou Cadastro Pessoa Física - CPF (Cópia)",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam dictum faucibus diam in vestibulum. Fusce tempor ligula nec nunc porttitor, id condimentum purus interdum.",
          whereToGet:
            "Pellentesque nec diam ac tortor convallis fringilla vel vel dolor. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.",
          reponsability: "Lorem ipsum dolor sit ame",
        },
        {
          name: "Estudo Ambiental correlato",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam dictum faucibus diam in vestibulum. Fusce tempor ligula nec nunc porttitor, id condimentum purus interdum.",
          whereToGet:
            "Pellentesque nec diam ac tortor convallis fringilla vel vel dolor. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.",
          reponsability: "Lorem ipsum dolor sit ame",
        },
        {
          name: "Plano de Recuperação de Área Degradada - PRAD",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam dictum faucibus diam in vestibulum. Fusce tempor ligula nec nunc porttitor, id condimentum purus interdum.",
          whereToGet:
            "Pellentesque nec diam ac tortor convallis fringilla vel vel dolor. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.",
          reponsability: "Lorem ipsum dolor sit ame",
        },
        {
          name: "Manifestação da concessionária de abastecimento de água relativa a restrições e/ou afastamentos mínimos do ponto de captação (Cópia).",
          description:
            "Lorem ipsum dolor sit amet, consectetur adipiscing elit. Nullam dictum faucibus diam in vestibulum. Fusce tempor ligula nec nunc porttitor, id condimentum purus interdum.",
          whereToGet:
            "Pellentesque nec diam ac tortor convallis fringilla vel vel dolor. Orci varius natoque penatibus et magnis dis parturient montes, nascetur ridiculus mus.",
          reponsability: "Lorem ipsum dolor sit ame",
        },
      ],
      clientInfo: {
        name: "John Doe",
        activity: "00.10.00 - Lavra a céu aberto com desmonte por explosivo.",
        licencingType: "Licença prévia",
        address: "Itajai - SC",
      },
    };
  },
  components: {
    DocumentView,
    CardDefault,
  },
};
</script>

<style>
.btnEdit {
  background: #5d8d49;
  color: #ffff;
  text-transform: none;
}

.options {
  padding: 10px;
  text-align: left;
}
</style>