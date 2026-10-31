# 🐑 Pasto das Ovelhas

Simulação 3D (Three.js) de um pasto com 10 ovelhas que dependem de ti: dá-lhes feno e água, ou morrem.

- **Cérebro estilo connectome** (inspirado nos simuladores do connectome da mosca da fruta): 235 neurónios
  (sentidos → impulsos → neurónios de conjunção → motores, mais um reservatório de 180 neurónios),
  ~1550 sinapses, mesma cablagem para todas e pesos/personalidade individuais. O painel mostra a atividade em tempo real.
- **Decisões consoante as necessidades**: uma camada de neurónios de decisão (Beber, Comer, Dormir, Descansar)
  compete por inibição mútua. A sede tem prioridade sobre a fome; cada decisão tem compromisso (auto-excitação):
  começa a beber com ~50% de água e só pára perto de 90%. Sem relva vão ao feno; de barriga cheia deitam-se a ruminar
  ou exploram; à noite dormem. O painel mostra os objetivos em competição e o motivo de cada decisão.
- **Pegar nas ovelhas**: arrasta-as para outro sítio (ficam assustadas quando as largas).
- **Dia/noite e meteorologia reais** pela tua localização (Open-Meteo): chuva, neve, nevoeiro, trovoada.
- **Tempo real**: fome 100→0 em ~10 h, sede em ~8 h; sem comida/água morrem em ~12 h. O jogo é guardado e o tempo
  em que estiveste fora é simulado.
- Mundo cartoon com o horizonte pintado e bordas em estilo pintura a óleo.

## Correr

Um único ficheiro (`index.html`). Serve-o localmente (a geolocalização precisa de um contexto seguro):

```bash
python -m http.server 5173
```

e abre http://localhost:5173.
