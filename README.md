# BancaPro

Controle de banca e apostas esportivas. Arquivo único, roda offline, sem cadastro.

**Demo:** https://sandrolimadf1984.github.io/bancapro/

## Por que existe

Eu anotava minhas apostas numa planilha e vivia perdendo o controle de quanto
era depósito e quanto era bônus — que rendem de forma diferente e não faz sentido
somar no mesmo saldo. Nenhum app que testei separava isso direito, então fiz o meu.

Ele **não aposta nada**: não conecta em casa de aposta, não tem link pra lugar
nenhum, não movimenta dinheiro. Você aposta onde já aposta e registra aqui.

## O que faz

- Banca separada em depósito e bônus, com saldo de cada um
- Bilhete simples, múltipla e criar aposta
- Múltipla resolvida jogo a jogo (green / red / null por partida)
- Cash out
- Mercados guiados: 1X2, over/under (total, tempos, casa, visitante), handicaps,
  dupla chance, escanteios, cartões, placar exato, jogador pra marcar
- Times por país e campeonato, com cadastro próprio
- Estatísticas: lucro, ROI, yield, taxa de acerto, evolução da banca, desempenho
  por mercado / casa / faixa de odd / dia da semana
- Metas, agenda de jogos, stake sugerida, stop loss e stop win
- PIN
- PT / EN / ES

## Stack

HTML, CSS e JavaScript puro, sem framework e sem build. O app inteiro é um
`index.html` — Chart.js vai embutido no arquivo, então funciona offline e dá pra
mandar por WhatsApp que abre. Persistência em `localStorage`.

O Android é empacotado com Capacitor. Atualização de conteúdo vai por OTA
(`@capgo/capacitor-updater`), lendo o `version.json` daqui do repositório —
correção de tela não precisa esperar revisão da loja.

```
index.html                    app inteiro
politica-de-privacidade.html
version.json                  versão publicada + checksum do bundle
bundles/                      pacotes de atualização
```

## Decisões que valem nota

**Arquivo único.** Foi de propósito. Sem npm, sem bundler, sem servidor —
abre com dois cliques em qualquer lugar e continua funcionando daqui a cinco anos.

**i18n por camada.** Traduzo o DOM depois de renderizar, em vez de trocar tudo
por chaves. O português continua sendo a fonte, então nenhum cálculo ou `value`
de `<select>` muda junto quando troca de idioma.

**Drawer com `margin-left`, não `transform`.** No WebView do Android a animação
de transform travava no meio e o menu abria cortado. Com margin o layout é
recalculado e não acontece.

## Privacidade

Não coleta, não envia, não compartilha nada. Sem servidor, sem login, sem
rastreamento, sem anúncio. Os dados ficam no aparelho de quem usa.

## Aviso

Maiores de 18 anos. Aposte com responsabilidade e só o que puder perder.
CVV: 188 (gratuito, 24h).

---

Sandro Lima — [@sandrolimadf1984](https://github.com/sandrolimadf1984)
