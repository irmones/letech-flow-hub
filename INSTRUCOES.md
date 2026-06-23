# Como subir o portfólio no GitHub

## Passo 1 — Criar o repositório

1. Acesse github.com e logue na conta `irmones`
2. Clique em **New repository**
3. Preencha:
   - **Repository name:** `letech-flow-hub`
   - **Description:** ERP empresarial desenvolvido para a Letech Energia
   - **Visibility:** Public
4. **NÃO** marque nenhuma opção de inicialização (sem README, sem .gitignore)
5. Clique em **Create repository**

---

## Passo 2 — Adicionar as screenshots

Antes de subir, tire prints das seguintes telas do sistema (zoom 80% no browser):

| Arquivo | Tela |
|---|---|
| `assets/screenshots/01-dashboard.png` | Dashboard principal |
| `assets/screenshots/02-dre.png` | Financeiro → DRE |
| `assets/screenshots/03-os-detalhe.png` | Detalhe de uma OS com equipe e gastos |
| `assets/screenshots/04-proposta-pdf.png` | PDF de proposta gerado |
| `assets/screenshots/05-locacoes.png` | Lista de locações com badges |
| `assets/screenshots/06-frequencia.png` | Tabela de frequência da equipe |
| `assets/screenshots/07-frota.png` | Frota com histórico |

Salve os arquivos exatamente com esses nomes dentro da pasta `assets/screenshots/`.

---

## Passo 3 — Subir os arquivos

Após adicionar as screenshots, suba tudo pelo terminal:

```bash
cd portfolio-danilo
git init
git add .
git commit -m "feat: portfolio ERP Letech Flow Hub"
git branch -M main
git remote add origin https://github.com/irmones/letech-flow-hub.git
git push -u origin main
```

---

## Resultado

O repositório ficará em:
**https://github.com/irmones/letech-flow-hub**

O README aparece automaticamente na página principal do repo.
