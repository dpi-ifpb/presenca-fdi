# Lista de presença — Reunião Ordinária do FDI (Reditec 2026)

Formulário web + Planilha Google. As respostas ficam na **sua** planilha; os participantes não precisam de login.

## Instalação (cerca de 5 minutos)

1. Crie uma Planilha Google nova (ex.: "FDI 2026 – Presenças").
2. Menu **Extensões › Apps Script**.
3. No editor:
   - Substitua o conteúdo de `Código.gs` pelo de **Code.gs**.
   - **+ › HTML** → nome `Index` → cole **Index.html**.
   - **+ › HTML** → nome `Logo` → cole **Logo.html** (é só o logo em base64).
4. Selecione a função `configurarPlanilha` e clique em **Executar** (autorize na 1ª vez).
   Serão criadas as abas **Instituicoes**, **Membros** (41 membros) e **Presencas**.
5. **Implantar › Nova implantação › Tipo: App da Web**
   - Executar como: **Eu**
   - Quem pode acessar: **Qualquer pessoa**
   → copie o URL `.../exec`.
6. Recarregue a planilha: aparece o menu **Lista de presença**.
   - **Mostrar QR Code do formulário** — QR do link publicado.
   - **Gerar PDFs por dia** — um PDF por dia, na pasta do Drive "FDI 2026 - Listas de presença" (gerar de novo substitui).

## Ajustes

- **Datas do evento**: `CONFIG.DIAS` no início do Code.gs.
- **E-mails dos membros**: preencha a coluna C da aba *Membros*; o formulário passa a sugerir o e-mail ao escolher o nome.
- **Novos membros / instituições**: basta incluir linhas nas abas *Membros* e *Instituicoes* (sem republicar).
- Alterou **Code.gs ou Index.html**? *Implantar › Gerenciar implantações › editar › Versão: Nova versão* (mantém o mesmo link/QR).

## Regras do formulário

- Data do dia vem marcada e travada; as outras ficam desabilitadas.
- "Registro de presença retroativa" libera os dias anteriores (nunca os futuros) e sugere informar o motivo na observação.
- Mesma pessoa no mesmo dia não é gravada duas vezes (avisa "já constava na lista").
- Os e-mails da base não ficam no código da página; são consultados só quando o nome é escolhido.
