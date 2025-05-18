# 📄✨ Assistente de Análise de Texto Rápida com Gemini ✨📄

Olá! Este é um projeto simples feito em Python que usa a inteligência artificial Gemini do Google para te ajudar a entender textos longos rapidinho!

Pensa nele como um super assistente que lê por você e te entrega as partes mais importantes.

## O que ele faz?

Este assistente tem 3 "ajudantes" ou "agentes" que trabalham juntos:

1.  **Resumidor:** Lê o texto e faz um resumo curtinho para você.
2.  **Extrator de Ações:** Procura no texto por coisas que você precisa fazer (tarefas, compromissos).
3.  **Extrator de Informações Chave:** Encontra nomes de pessoas, datas, lugares e outros dados importantes no texto.

Tudo isso aparece organizado em uma pagininha fácil de usar, feita com a ferramenta Gradio.

## Como usar o Projeto?

Para usar este assistente, você vai precisar:

1.  Ter uma conta no Google e acesso ao **Google Colab** (é de graça!).
2.  Ter uma **chave de API do Google Gemini**. Você pode conseguir uma de graça no [Google AI Studio](https://aistudio.google.com/app/apikey). **Guarde sua chave em segredo!**
3.  O código deste projeto (o arquivo `.ipynb` que você baixou).

Passos:

1.  Abra o Google Colab ([https://colab.research.google.com/](https://colab.research.google.com/)).
2.  No Colab, clique em "Arquivo" (ou File) -> "Fazer upload de notebook" (ou Upload notebook) e escolha o arquivo `.ipynb` que você baixou deste GitHub.
3.  O notebook vai abrir. Ele é dividido em partes (células de código).
4.  Rode a **primeira célula** para instalar as ferramentas e configurar o Gemini. Ele vai pedir sua chave secreta - cole ela e aperte Enter. (Sua chave NÃO fica salva no arquivo!).
5.  Rode a **segunda célula** para carregar o "cérebro" do assistente (a função que faz o trabalho).
6.  Rode a **terceira célula** para ligar a pagininha mágica do Gradio. Uma interface vai aparecer logo abaixo ou em um link.
7.  Na pagininha, cole o texto que você quer analisar (lembre-se do limite de aproximadamente **2000 caracteres**) e clique em "Submit".
8.  Os resultados aparecerão nas caixas abaixo!

## Coisas Importantes:

*   **Limite de Texto:** A IA (modelo Gemini Flash) é super rápida, mas tem um limite de texto que consegue processar por vez para não dar erro ou demorar demais. O limite neste projeto é de aproximadamente **2000 caracteres**. Se colar mais, ele avisará.
*   **Timeouts:** Com textos complexos, mesmo dentro do limite, a IA pode demorar mais de 60 segundos. Se isso acontecer, uma mensagem de "timeout" aparecerá. Tentar reduzir AINDA MAIS o texto ou simplificar as frases pode ajudar. Reiniciar o "Ambiente de execução" no Colab (menu lá em cima) também pode resolver problemas temporários.
*   **Finalizar a Sessão:** Para limpar a interface e parar de processar novos textos pela pagininha, você pode digitar `FINALIZAR_SESSAO` na caixa de texto e clicar em Submit.
*   **Parar Tudo:** Para desligar *completamente* o assistente e o servidor que roda a pagininha no Colab, você precisa clicar no botão quadrado [■] que aparece do lado da terceira célula enquanto ela está rodando no Colab.

## Sobre a Chave Gemini

Sua chave de API é secreta e é a forma que o Google tem de saber que é você usando o serviço (e controlar o uso, que geralmente tem um nível gratuito bem generoso!).

Este projeto usa `getpass` para pedir sua chave quando você roda a primeira célula. Isso significa que a chave **não fica escrita no código do notebook** depois que você roda, e **não será salva no arquivo `.ipynb`** que você subiu para o GitHub.

**NUNCA** digite sua chave API diretamente no código e salve em um arquivo público!

## Feito com

*   Python
*   Google Colab
*   Google Gemini API (modelo `gemini-1.0-flash`)
*   Biblioteca Gradio

Espero que goste e que seja útil! 😊
