# PRD — Jogo: Letra Inicial da Vogal

## Visão Geral

Jogo educacional para crianças identificarem a letra inicial de palavras, trabalhando as 5 vogais (A, E, I, O, U).

---

## Tecnologia

- **Plataforma:** HTML + CSS + JavaScript (abre no navegador, sem instalação)
- **Arquivo principal:** `index.html`

---

## Layout da Tela

- **Esquerda:** Personagem (placeholder por enquanto)
- **Centro:** Imagem da palavra em destaque
- **Inferior:** 3 botões de letras em linha horizontal

---

## Mecânica do Jogo

### Palavras
- Fonte: todos os arquivos `.jpg` da pasta `img/` (330 imagens)
- Ordem: aleatória, embaralhada a cada sessão, a cada nova sessão sorteia uma outra palavra que não inicie com a mesma letra da palavra anterior
- Nome da palavra derivado do nome do arquivo:
  - Remover sufixo numérico final (`espiga2` → `espiga`)
  - Trocar `_` por espaço para exibição (`escova_de_dente` → `escova de dente`)
  - Manter underscores no nome do arquivo de áudio (`audio/escova_de_dente.mp3`)
- Vogal correta = primeira letra do nome base do arquivo (case-insensitive)

### Opções de Letras
- 3 botões exibidos: a vogal correta + 2 distratoras aleatórias entre as outras 4 vogais
- Posições embaralhadas a cada rodada (a resposta correta não fica sempre no mesmo lugar)
- Estilo: botões CSS (sem arquivos de imagem) — fonte grande, cor vibrante, borda arredondada

### Interação
- Clicar no botão da letra na tela **OU** pressionar a tecla correspondente no teclado (A, E, I, O, U)

---

## Fluxo de uma Rodada

1. Personagem "fala" o enunciado: **"Seleciona a letra inicial da palavra"**
2. Personagem "fala" o nome da palavra
3. Imagem da palavra é exibida ao centro
4. 3 botões de letras aparecem na parte inferior
5. Aluno escolhe uma letra
6. Aparece uma animação da imagem e fala novamente o nome da palavra

---

## Feedback de Resposta

| Situação | Ação |
|----------|------|
| **Acerto** | Animação na letra + som curto de acerto → avança após ~2s |
| **1º erro** | Animação na letra + som curto de erro → aluno tenta novamente |
| **2º erro** | Repete o áudio da palavra + animação destacando a letra correta → avança após ~2s |

---

## Áudio

### Enunciado e Nome da Palavra
- **Primário:** arquivo `.mp3` em `audio/<baseName>.mp3` (quando disponível)
- **Fallback:** Web Speech API (voz sintética do navegador) — o jogo funciona sem arquivos de áudio

### Sons de Acerto/Erro
- Gerados via **Web Audio API** (sem arquivos externos)

### Formato dos Arquivos de Áudio das Palavras
- Extensão: `.mp3`
- Nome: mesmo base do arquivo de imagem (sem número final, com underscores preservados)
  - Ex: `img/espiga2.jpg` → `audio/espiga.mp3`
  - Ex: `img/escova_de_dente.jpg` → `audio/escova_de_dente.mp3`

---

## Tela de Conclusão (Parabéns)

- Exibida quando todas as palavras da rodada forem apresentadas
- Mostra: mensagem de parabéns + quantidade de palavras acertadas
- Botão **"Jogar novamente"** — embaralha e reinicia

---

## Estrutura de Arquivos

```
ativ_alex/
├── index.html          ← jogo completo
├── img/                ← 330 imagens .jpg das palavras
└── audio/              ← arquivos .mp3 (adicionados posteriormente)
```

---

## Lista de Imagens por Vogal

### A (157 imagens)
abacate (×2), abacaxi (×2), abaixa lingua, abajur, abelha (×2), abelhas, abobora (×2), abraco, abril, abrir, acacia, academia, acai, acenar, acender, acerola, acordar, acougue, acrobata, acucar, acucareiro, adulto, adultos, aeroporto, afundar, agosto, agriao, agua, aguape, aguaviva, aguia cinzenta, aguia, agulha, aipo, ajuda, alaranjado, albatroz, albatroz real, album, alca, alce, aldeia, alecrim, alema, alerta, alfabeto, alface dagua, alface, alfavaca, alfinete, alga, algas, algema, algemas, algodao, alho, alicate, alice, alimento, alimentos, almoco, almondega, alossauro, altofalante, alvo, amarelinha, amarelo, amazonsaurus, ambulancia, amendoim, amigo, amigos, amor perfeito, amor, amora, ana da esquina, anao, anchova, ancora, andar, andorinha, androide, anel, animais, animal, aniversario, anoes, anos, anta cachorro, anta, antilope, anzol, apagar, apartamento, apartamentos, apatossauro, apito, aquario, aquecer, ar, arames, aranha (×2), arara (×2), arara azul, arara caninde, ararajuba, ararinha azul, arbusto, arco, arcoiris, areia, argila, ariranha, armadilha, armador, armazem, armazens, aro, arpao, arquiteto, arquivo, arraia, arroz, arruda, artesao, arvore, arvores, asa, asinhas (×2), assar, assento, astronauta, atleta, ator, atum, auto escola, autodromo, ave, avental, aves, avestruz, aviao (×2), aviaozinho, aviario, avo, azaleia, azeite, azul, azulejo

### E (94 imagens)
eclipse, edificio, egua, elastico, elefante (×2), eletricista, elevador, elfos, ema, email, emas, embauba, emilia, empada, empurrar, encanador, encapo, encolher, enfermeiro, engenheiro, enterrar, envelope, enxada, erva cidreira, escada, escama, escamas, escapo, escaravelho, escola, esconde esconde, escorpiao (×2), escorregador, escoteiro, escoteiros, escova de cabelo, escova de dente, escova, escovas, escrever, escudo, escultura, escuridao, esfera, esfiapo, esmalte, esmeralda, espada, espaguete, espalhar, espantalho (×2), esparadrapo, espatula, espelho, espetinho, espiga (×2), espinafre, espinha, espinho, espinhos, espinossauro, espiral, espirro, esponja, esporte, espremer, espuma, esqueleto, esqui aquatico, esquilo, esquimo (×2), esquina, estante, estantes, estatua, estegossauro, estetoscopio, estevia, estojo, estourar, estrada, estrela (×2), estrela do mar, estreladomar, etiqueta, eucalipto, explosao, extintor

### I (22 imagens)
iara, iate, ideia, iglu, igreja, igrejas, indigena, indio (×2), inseto, instrumento, instrumentos, interruptor, inundar, inverno, iogurte, ioio, irere, iris, irma, irmao, isca

### O (43 imagens)
oasis, obelisco, oboe, obraprima, oca, ocas, oceano, ocre, oculos, oficina, oleo, olho, olhos, ombro, onca boi, onca parda, onca pintada, onca preta, onca, onda, ondas, onibus, orangotango, orca, orelha, orelhas, orquidea, osso, ossos, ostra, otoscopio, ourico do mar, ourico preto, ourico, ouro, outono, outubro, oval, ovelha (×2), ovelhas, ovo, ovos

### U (14 imagens)
uirapuru, umbigo, unaysaurus, unha, unhas, unicornio, uniforme, universo, urso de pelucia, urso, urubu rei, urubu, utensilio, utensilios
