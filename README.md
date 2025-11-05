# JS-Drum-Kit

Um pequeno projeto interativo em JavaScript que simula uma **bateria virtual**.  
Ao pressionar determinadas teclas do teclado, sons diferentes são reproduzidos e um efeito visual destaca a tecla correspondente na tela.

---

## 🚀 Demonstração

![JS Drum Kit](https://media.giphy.com/media/26gR1yJvK0O4eYv4Q/giphy.gif)

*(exemplo ilustrativo — não é a versão exata do projeto)*

---

## 🧠 Conceitos abordados

Este projeto foi desenvolvido como prática de **JavaScript e manipulação do DOM**, inspirado no clássico exercício do [Wes Bos – JavaScript30](https://javascript30.com/).

Durante o desenvolvimento, são aplicados conceitos como:

- Eventos de teclado (`keydown`)
- Manipulação do DOM com `querySelector` e `classList`
- Controle de reprodução de áudio com o elemento `<audio>`
- Uso de `data-* attributes`
- Efeitos visuais com **CSS transitions**

---

## 🧩 Estrutura do projeto

DRUMKIT/
├── index.html
├── style.css
├── sound/
│   ├── clap.wav
│   ├── hihat.wav
│   ├── kick.wav
│   ├── openhat.wav
│   ├── boom.wav
│   ├── ride.wav
│   ├── snare.wav
│   ├── tom.wav
│   └── tink.wav
└── README.md

## 🎮 Como funciona

1. Cada tecla exibida na tela tem um atributo `data-key` com o código da tecla do teclado.
2. Quando o usuário pressiona uma tecla (`keydown`):
   - O JavaScript identifica o `keyCode` correspondente.
   - Busca o elemento `<audio>` com o mesmo `data-key`.
   - Reinicia o som (`audio.currentTime = 0`) e o reproduz.
   - Adiciona a classe `.playing` na tecla correspondente.
3. Quando a transição CSS termina, o evento `transitionend` remove o destaque visual.

---

## 💻 Como executar

1. Baixe o projeto ou clone o repositório:
   ```bash
   git clone https://github.com/seuusuario/js-drum-kit.git
