# 📊 BancaPro — Gestão de Apostas

Aplicativo web (arquivo único, funciona offline) para gerir apostas esportivas de forma
profissional: banca com **depósito e bônus**, bilhetes **simples, múltiplas e criar aposta**,
resolução **jogo a jogo** (Green/Red/Null), **Cash Out**, estatísticas, metas e muito mais.
Os dados ficam salvos **no próprio aparelho** de cada pessoa (no navegador), então é seguro
compartilhar o mesmo arquivo com qualquer um.

---

## ✨ O que ele faz

- **Banca (depósito + bônus):** saldo total em destaque e, abaixo, saldo de depósito e de
  bônus separados. Ao apostar, você escolhe de qual conta sai o valor.
- **Tipos de aposta:** Simples, Múltipla e Criar Aposta.
- **Seletores inteligentes:** País → Campeonato, e times por competição (com opção de
  digitar/excluir e memorização por campeonato).
- **Seleção por mercado:** Resultado Final (1X2), Over/Under (com Casa/Visitante), Handicaps,
  Dupla Chance, Escanteios, Cartões, Placar Exato, Jogador p/ Marcar, Aposta de longo prazo e Especiais.
- **Múltipla resolvida jogo a jogo:** marque Green/Red/Null em cada jogo; um Red encerra como
  perdida; ajuste de retorno quando um jogo é anulado.
- **Cash Out** em simples e múltiplas.
- **Estatísticas, metas, agenda e um resumo de IA** com insights do seu desempenho.

---

## ▶️ Como usar

**Opção 1 — abrir direto:** baixe o `index.html` e abra com dois cliques no navegador
(Chrome, Edge, etc.). Funciona no computador e no celular.

**Opção 2 — publicar na internet (GitHub Pages):** siga o passo a passo abaixo para ter um
**link** que você abre de qualquer lugar e compartilha com outras pessoas.

---

## 🌐 Publicar no GitHub Pages (passo a passo, bem simples)

> Resultado: um endereço tipo `https://sandrolimadf1984.github.io/bancapro/` que abre o app.

1. Crie uma conta em **https://github.com** (se ainda não tiver).
2. Clique no **+** (canto superior direito) → **New repository**.
3. Em **Repository name**, escreva `bancapro`. Marque **Public**. Clique **Create repository**.
4. Na página do repositório novo, clique em **“uploading an existing file”** (ou
   **Add file → Upload files**).
5. **Arraste o arquivo `index.html`** para a área de upload. Desça e clique **Commit changes**.
6. No menu de cima do repositório, vá em **Settings** (Configurações).
7. No menu da esquerda, clique em **Pages**.
8. Em **Branch**, escolha **main** e pasta **/(root)**. Clique **Save**.
9. Espere ~1 minuto e recarregue a página. Vai aparecer:
   **“Your site is live at https://sandrolimadf1984.github.io/bancapro/”**.
10. Pronto! Esse é o seu link. É só abrir e compartilhar. 🎉

**Para atualizar o app depois:** repita o passo 4–5 enviando o `index.html` novo (o GitHub
pergunta se quer substituir — confirme). Em 1–2 minutos o link já mostra a versão nova.

---

## 📱 Quer transformar em APK (Google Play)?

Existe um projeto separado já pronto (Capacitor) com um guia passo a passo para gerar o APK
e publicar na Play Store. Procure o arquivo **`bancapro-cap.zip`** e o **guia** que
acompanham este projeto.

---

## 🔒 Privacidade dos dados

Cada pessoa que abrir o app tem os **próprios dados**, guardados apenas no navegador do
aparelho dela (armazenamento local). Nada é enviado para servidores. Se limpar os dados do
navegador, o histórico é apagado.

---

## 🗂️ Estrutura

```
bancapro/
├── index.html                    ← o aplicativo inteiro
├── politica-de-privacidade.html  ← exigida pela Google Play
├── version.json                  ← avisa os apps que há versão nova
├── bundles/                      ← pacotes de atualização (.zip)
└── README.md                     ← este arquivo
```

## 🔄 Atualizações automáticas

O app instalado no celular consulta o `version.json` deste repositório. Quando a versão
publicada aqui é maior que a instalada, o app mostra **"Nova versão disponível"** e se
atualiza sozinho — sem passar pela loja.

Feito com carinho para uso pessoal. ⚽📈
