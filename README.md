# Boas vindas ao repositório do projeto JavaScript Basics Quiz!

Aqui você vai encontrar os detalhes para desenvolver um quiz interativo que ajuda no aprendizado de conceitos fundamentais de JavaScript como loops, HOFs, condições e arrow functions.

# Entregáveis

Para entregar seu projeto, crie um _Pull Request_ contendo:
- `index.html` (estrutura da página)
- `style.css` (estilização)
- `script.js` (lógica do quiz)

---

## Requisitos Obrigatórios:

Implemente um quiz com 5 perguntas sobre JavaScript básico. O projeto deve incluir:

---

## Requisitos do Projeto

### 1 - O site deve ter um título claro
- **ID:** `quiz-title`
- Deve exibir "JavaScript Basics Quiz"

### 2 - Exibir área de perguntas
- **ID:** `question-container`
- Deve mostrar a pergunta atual com formatação clara

### 3 - Opções de resposta clicáveis
- **ID:** `options-container`
- 4 botões por pergunta com **class** `option-btn`
- Gerar opções dinamicamente via JavaScript

### 4 - Feedback imediato
- **ID:** `feedback`
- Exibir "Clique para responder!" inicialmente
- Mostrar "Correto!" ou "Errado!" após resposta
- Atualizar feedback sem recarregar a página

### 5 - Controle de fluxo
- Progresso automático para próxima pergunta após resposta
- Usar `setTimeout` para transição de 1.5s entre perguntas

### 6 - Sistema de pontuação
- **ID:** `score`
- Iniciar em 0 pontos
- +10 pontos por resposta correta
- Atualizar pontuação em tempo real

### 7 - Tela final
- **ID:** `end-screen`
- Mostrar pontuação final
- Botão "Reiniciar Quiz" com **ID** `restart-btn`

---

## Requisitos Bônus:

### 8 - Timer por pergunta
- **ID:** `timer`
- Contagem regressiva de 30s por pergunta
- Tempo esgotado = resposta errada

### 9 - Progresso visual
- **ID:** `progress`
- Barra ou texto mostrando (pergunta atual/5)

### 10 - Local Storage
- Salvar recorde máximo
- Exibir "Recorde: X pontos" com **ID** `high-score`

### 11 - Integração com QuizAPI (Bônus Avançado)
- **ID:** `api-integration`
- Utilize a [QuizAPI.io](https://quizapi.io/docs/1.0/overview) para buscar perguntas dinâmicas

**Implementação com Axios:**

1. Adicione o Axios no HTML:
```html
<script src="https://cdn.jsdelivr.net/npm/axios/dist/axios.min.js"></script>


```

2. exemplo de uso da API com axios:
```javascript
const response = await axios.get('https://quizapi.io/api/v1/questions', {
  params: {
    apiKey: API_KEY,
    category: 'javascript',
    difficulty: 'easy',
    limit: 5
  }
});
```

#### Como usar:
**API**
Registre-se no QuizAPI para obter uma chave gratuita

Substitua SUA_CHAVE_AQUI pela sua chave

**Axios**
https://axios-http.com/ptbr/docs/example

https://dev.to/julianafelix/como-consumir-api-com-js-puro-e-axios-em-3-passos-3jnf