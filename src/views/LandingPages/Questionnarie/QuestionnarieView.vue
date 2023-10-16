<script>
import { FlowForm, QuestionModel, QuestionType, ChoiceOption, LanguageModel } from '@ditdot-dev/vue-flow-form';
import { onMounted } from "vue";
import setMaterialInput from "@/assets/js/material-input";

onMounted(() => {
  setMaterialInput();
});

export default {
  name: 'example',
  components: {
    FlowForm
  },
  data() {
    return {
      language: new LanguageModel({
        thankYouText: 'Obrigado!'
        // Your language definitions here (optional).
        // You can leave out this prop if you want to use the default definitions.
      }),
      questions: [
        // QuestionModel array
        new QuestionModel({
          id: 'portuguese-1',
          title: 'Assinale a opção em que todas as palavras estão grafadas corretamente:',
          type: QuestionType.MultipleChoice,
          options: [
            new ChoiceOption({
              label: 'asteristico – jiló – xampu – chinesa.'
            }),
            new ChoiceOption({
              label: 'magestade - maizena - cerejeira - ferruginoso.'
            }),
            new ChoiceOption({
              label: 'entitulado - gerimum - sargeta - tigela.'
            }),
            new ChoiceOption({
              label: 'rigidez - exceção - megera - submersão.'
            }),
            new ChoiceOption({
              label: 'pagem - ogeriza - diligência - gorgeta.'
            })
          ]
        })
        ,new QuestionModel({
          id: 'portuguese-1',
          title: 'Assinale a alternativa correta quanto à concordância verbal:',
          type: QuestionType.MultipleChoice,
          options: [
            new ChoiceOption({
              label: 'É cinco horas da tarde.'
            }),
            new ChoiceOption({
              label: 'Sou eu quem primeiro sai.'
            }),
            new ChoiceOption({
              label: 'Da cidade à praia é dois quilômetros.'
            }),
            new ChoiceOption({
              label: 'Dois metros de tecido são pouco.'
            }),
            new ChoiceOption({
              label: 'A gente fomos juntos para o parque.'
            })
          ]
        })
        ,new QuestionModel({
          id: 'math-1',
          title: 'Um quadro branco tem 1,20 m de altura por 3,30 m de comprimento, qual é área do mesmo em m²?',
          type: QuestionType.MultipleChoice,
          options: [
            new ChoiceOption({
              label: '1,2'
            }),
            new ChoiceOption({
              label: '3,35'
            }),
            new ChoiceOption({
              label: '5,5'
            }),
            new ChoiceOption({
              label: '3,3'
            }),
            new ChoiceOption({
              label: '3,96'
            })
          ]
        })
        ,new QuestionModel({
          id: 'math-2',
          title: 'Julia, filha de Elisandra, está aprendendo frações e números decimais. Ela sabe que A = 5/25; B = 0,012; C = 0,43/4. Do exposto é CORRETO afirmar:',
          type: QuestionType.MultipleChoice,
          options: [
            new ChoiceOption({
              label: 'B é maior que A e menor que C'
            }),
            new ChoiceOption({
              label: 'A+B = 3C+ 0,1'
            }),
            new ChoiceOption({
              label: 'A-B=C'
            }),
            new ChoiceOption({
              label: 'A é maior que C-B.'
            }),
            new ChoiceOption({
              label: 'A é igual a C-2B.'
            })
          ]
        })
        ,new QuestionModel({
          id: 'language-1',
          title: '________ an auditorium big enough for 80 people in this building?',
          type: QuestionType.MultipleChoice,
          options: [
            new ChoiceOption({
              label: 'Is'
            }),
            new ChoiceOption({
              label: 'There is'
            }),
            new ChoiceOption({
              label: 'Is it'
            }),
            new ChoiceOption({
              label: 'Is there'
            })
          ]
        })
        ,new QuestionModel({
          id: 'language-2',
          title: 'Japanese is __________ English.',
          type: QuestionType.MultipleChoice,
          options: [
            new ChoiceOption({
              label: 'much harder than'
            }),
            new ChoiceOption({
              label: 'very hard than'
            }),
            new ChoiceOption({
              label: 'harder of that'
            }),
            new ChoiceOption({
              label: 'a more hard than'
            })
          ]
        })
      ]
    }
  }
}
</script>

<template>
    <flow-form v-bind:questions="questions" v-bind:language="language" />
    <link rel="stylesheet" href="https://unpkg.com/@ditdot-dev/vue-flow-form@2.3.2/dist/vue-flow-form.min.css">
    <link rel="stylesheet" href="https://unpkg.com/@ditdot-dev/vue-flow-form@2.3.2/dist/vue-flow-form.theme-minimal.min.css">
    <link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;900&amp;display=swap">
  
</template>
  
<style>
.f-text {
  font-size: 2vw
}

.vff {
  width: 100%;
  padding: 0 10%;
  margin: 4vh 0 100px !important;

}

.vff .fh2, .vff h2 {
    line-height: 1 !important;
}
/* #b81366 #4caf50 #41b883 */

</style>