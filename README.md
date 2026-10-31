# 🐑 Pasto das Ovelhas

Simulação 3D (Three.js) de um pasto com até 10 ovelhas que dependem de ti — em tempo real, ligada à tua localização.

## O cérebro
- **Connectome estilo mosca da fruta**: ~275 neurónios (sentidos → impulsos → decisões → conjunções → motores, mais um
  reservatório de 180 neurónios) e ~1650 sinapses. Mesma cablagem para todas; os pesos são o **genoma** de cada ovelha.
- **Decisões consoante as necessidades**: Beber, Comer, Dormir, Descansar/ruminar e Abrigo competem por inibição mútua,
  com compromisso (começa a beber com ~50% e só pára perto de 90%). Fugir (raposa, cão, desconfiança) anula tudo.
- **Memória espacial**: cada ovelha lembra-se de onde viu boa relva (mapa mental visível no painel).
- **Aprendizagem**: pegar nela baixa a confiança; festas (carregar sem mexer) e encher os comedouros sobem-na.
  Quem confia vem ter com o rato; quem tem medo foge.
- **Hierarquia**: a mais dominante é a líder 👑 — as outras seguem-na e ela empurra mais nos comedouros.
- **Emoções visíveis**: orelhas para trás com medo, saltinhos dos borregos quando estão contentes.

## Biologia
- **Ciclo de vida**: borregos crescem até adultos em ~14 dias; idosas ficam mais lentas; morrem de velhice.
- **Reprodução com genética**: com um carneiro adulto e vagas livres, as ovelhas saudáveis engravidam (3 dias).
  O borrego herda sinapses do pai e da mãe com mutações — personalidade e cor (a lã negra é recessiva) passam aos filhos.
- **Lã** que cresce e se tosquia (dá dinheiro, mas sem lã passam frio no inverno; com muita lã sofrem com o calor).
- **Temperatura corporal**: frio, vento, chuva e calor; procuram o abrigo coberto ou a sombra da árvore.
- **Rúmen**: pastar enche o estômago, que digere devagar — de barriga cheia deitam-se a ruminar.
- **Doenças**: tosse (contagiosa), coxeira, parasitas — com sintomas visíveis (tosse, coxear, isolar-se). Trata-as.

## Mundo
- Dia/noite e meteorologia **reais** pela tua localização (Open-Meteo), **estações do ano** (folhas, neve, relva).
- Tipos de relva (erva, trevo mais nutritivo, flores), raposa à noite, **cão pastor** que podes guiar,
  cerca que o vento parte (e por onde fogem as ovelhas e entra a raposa).
- Sons: balidos, tosse, latidos, pássaros, grilos, vento, chuva e trovoada.

## Pastor
- Dinheiro: feno, sementes, tratamentos e reparações custam; a lã tosquiada rende. A água do poço é grátis.
- **Diário** com todos os acontecimentos e **gráficos** de vida/comida/água/rebanho/dinheiro.
- **Avisos** (🔔) no telemóvel/computador quando uma ovelha precisa de ti, com a página aberta noutro separador.
- O jogo é guardado no browser e o tempo em que estiveste fora é simulado (nascimentos, doenças, mortes…).

## Correr

Um único ficheiro (`index.html`). Serve-o localmente (a geolocalização precisa de um contexto seguro):

```bash
python -m http.server 5173
```

e abre http://localhost:5173.
