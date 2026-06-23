#
<p align="center">
  <img src="logo/logo_simulador.png" alt="Transit Simulator logo" width="220"/>
</p>

# Simulador Interativo de Trânsitos de Exoplanetas

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
[![Pages](https://img.shields.io/badge/demo-online-brightgreen)](https://icaromeidem.github.io/transit-simulator/)
[![Languages](https://img.shields.io/badge/idiomas-PT%20%7C%20EN%20%7C%20ES-blue)](#)

**Acesse o simulador:** [icaromeidem.github.io/transit-simulator](https://icaromeidem.github.io/transit-simulator/)

Um simulador interativo, gratuito e de código aberto, desenvolvido em HTML5 e JavaScript, para o ensino de trânsitos planetários e do escurecimento de limbo estelar. Permite manipular em tempo real os parâmetros físicos e orbitais de um sistema exoplanetário e observar imediatamente seus efeitos sobre a curva de luz.

---

## O que é o trânsito planetário e o escurecimento de limbo?

O método de trânsito é a técnica mais produtiva na detecção de exoplanetas, respondendo por cerca de 75% das descobertas confirmadas. Ele se baseia na observação da diminuição periódica do brilho de uma estrela causada pela passagem de um planeta em frente ao seu disco.

A interpretação precisa dessa curva de luz exige considerar o **escurecimento de limbo** (*limb darkening*): as bordas do disco estelar emitem menos luz do que o centro, devido à estrutura térmica da fotosfera. Esse efeito arredonda as fases de ingresso e egresso do trânsito e é essencial para a determinação correta do raio planetário — longe de ser um mero ruído a ser descartado.

Este simulador foi desenvolvido como produto didático para tornar esse fenômeno visualmente manipulável, permitindo que estudantes explorem como diferentes parâmetros estelares e planetários moldam o sinal observado.

---

## Funcionalidades

- **Parâmetros geométricos e orbitais:** raio do planeta, raio da estrela, parâmetro de impacto e distância orbital, todos ajustáveis por controles deslizantes
- **Classificação espectral automática:** o tipo espectral (O, B, A, F, G, K, M) é determinado a partir do raio estelar informado, atualizando cor, massa e coeficientes de escurecimento de limbo
- **Escurecimento de limbo ativável/desativável:** compare em tempo real a curva de luz com e sem o efeito, usando a lei quadrática de Claret (2000)
- **Física orbital real:** o tempo de trânsito é calculado a partir da Terceira Lei de Kepler, e não de uma escala de tempo arbitrária
- **Animação sincronizada:** a posição do planeta e o ponto correspondente na curva de luz avançam estritamente em paralelo, com controle de linha do tempo (*scrubbing*) e velocidade
- **Multilíngue:** interface disponível em Português, Inglês e Espanhol
- **Execução 100% no navegador:** sem instalação, sem plugins, compatível com computadores, tablets e celulares

---

## Como usar

1. Acesse [icaromeidem.github.io/transit-simulator](https://icaromeidem.github.io/transit-simulator/)
2. Ajuste os parâmetros do planeta e da estrela usando os controles deslizantes
3. Ative ou desative o escurecimento de limbo na caixa de seleção
4. Clique em **Início** para iniciar a animação, ou arraste a linha do tempo manualmente
5. Observe a curva de luz sendo construída em tempo real, sincronizada com a posição do planeta

Um tutorial detalhado, com a descrição de cada controle e atividades pedagógicas sugeridas, está disponível na [página de tutorial](https://icaromeidem.github.io/transit-simulator/tutorial.html) do simulador.

---

## Fundamentação física

O motor do simulador é descrito em detalhe no artigo associado a este projeto (ver [Citação](#citação) abaixo). Resumidamente:

- A profundidade do trânsito é calculada a partir da solução analítica de Mandel & Agol (2002) para a área de ocultação entre dois discos
- O escurecimento de limbo segue a lei quadrática de Claret (2000), com coeficientes $u_1$ e $u_2$ atribuídos por classe espectral
- O tempo de trânsito ($T_{14}$) é derivado da física orbital real do sistema, via Terceira Lei de Kepler
- A renderização visual do gradiente estelar usa a API Canvas do HTML5, por meio de gradientes radiais

---

## Limitações conhecidas

O simulador é uma ferramenta de caráter exploratório e conceitual, não voltada à análise observacional quantitativa. A versão atual não incorpora:

- Ruído fotométrico instrumental
- Variabilidade estelar (manchas, atividade magnética)
- Atmosferas planetárias
- O formalismo completo de Mandel & Agol para fontes obscurecidas (é usada uma aproximação simplificada de ponto único)

---

## Contribuindo

Sugestões, relatos de uso em sala de aula e propostas de atividades pedagógicas são muito bem-vindos. Um formulário para coleta de feedback da comunidade de educadores está disponível [aqui](#) *(em breve)*.

Para contribuir diretamente com o código, abra uma *issue* ou *pull request* neste repositório.

---

## Autoria

Desenvolvido por **Ícaro Meidem**¹ e **Marcelo Emílio**¹,²

¹ Observatório Nacional, Departamento de Astronomia
² Universidade Estadual de Ponta Grossa, Departamento de Física

---

## Citação

Se você utilizar este simulador em pesquisa, ensino ou material didático, por favor cite:

```bibtex
@article{meidem2026simulador,
  author  = {Meidem, Ícaro and Emílio, Marcelo},
  title   = {Simulador interativo de trânsitos de exoplanetas como ferramenta didática para o ensino de Física e Astronomia},
  journal = {Revista Brasileira de Ensino de Física},
  year    = {2026},
  volume  = {48},
  note    = {No prelo},
  url     = {https://github.com/icaromeidem/transit-simulator}
}
```

---

## Licença

MIT © Ícaro Meidem
