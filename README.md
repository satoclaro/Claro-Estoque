# Claro - Controle de Equipamentos Diário (Versão 25.0)

Aplicação web responsiva e 100% client-side (offline-first via `localStorage`) em **tema escuro**, desenvolvida para registro, conferência, rastreio de reversa e exportação diária de equipamentos de telecomunicações em campo.

---

## Principais Funcionalidades

- **Cadastro Rápido de Equipamentos**:
  - Número do Contrato / OS
  - Destino / Movimentação: **Cliente** (Instalação / Entrega) ou **Reversa** (Retirada / Devolução)
  - Tipo de Equipamento: `ONT (Fibra Óptica)`, `EMTA (Modem HFC)`, `Decoder TV 4K / HD`, `Smartcard (Cartão Nagra)`, `Chip / ICCID Móvel` e `Roteador Mesh Wi-Fi`
  - Detecção automática do tipo de equipamento com base no prefixo ou padrão do código lido.
- **Leitor Híbrido com Linha de Mira (Código de Barras + OCR)**:
  - Combina `BarcodeDetector` nativo, `html5-qrcode` (ZXing) e `Tesseract.js` (OCR) operando apenas sobre a área da linha vermelha de mira.
  - **Filtro Inteligente de Etiquetas**: Aceita automaticamente `CM MAC`, `CA ID` / `CAID`, `Smartcard` e `ICCID`, rejeitando códigos indesejados como `BOX S/N`, `S/N`, `Serial`, `EAN`, `WIFI 2G/5G MAC`, `EMTA MAC`, `MoCA MAC` e `MAC Ethernet`.
  - **Botão `🔓 Forçar Leitura`**: Captura e copia imediatamente qualquer código de barras ou texto na mira (em 0°, 90° ou 270°), ignorando todos os filtros de rejeição quando necessário.
  - **Controles de Câmera**: `📸 Ler Mira Agora`, `🔓 Forçar Leitura`, `🎯 Focar`, `🔦 Luz` (lanterna) e toque direto na tela da câmera para focar e capturar.
  - **Cópia Automática**: Todo código capturado é preenchido no formulário e copiado automaticamente para a área de transferência.
- **Controle de Reversa e Pesquisa**:
  - Marcação de entrega de reversa (`📅 Entregue`) com registro automático de data e hora (`✓ Entregue: DD/MM/AAAA HH:MM`).
  - Busca instantânea por MAC, CA ID, Contrato/OS ou Data.
- **Exportação de Relatórios**:
  - **Excel (CSV)** compatível com Microsoft Excel (UTF-8 com BOM e separador `;`).
  - **PDF** em paisagem (A4) gerado com `jsPDF` + `AutoTable`, respeitando os filtros de busca aplicados.

---

## Como Usar

1. Abra o arquivo `index.html` diretamente no navegador do celular ou computador (ou hospede como site estático / GitHub Pages).
2. Informe o **Número do Contrato / OS** e selecione a **Movimentação** (`Cliente` ou `Reversa`).
3. Toque em **📷 Ligar e Desligar Câmera**, alinhe a linha vermelha sobre o código desejado e aguarde a captura automática ou toque na tela / em **📸 Ler Mira Agora**.
   - Caso precise ler um código normalmente filtrado (como Serial ou outro MAC), utilize o botão **🔓 Forçar Leitura**.
4. Clique em **Salvar Equipamento** para armazenar o registro localmente no aparelho.
5. Utilize **📥 Baixar Excel (CSV)** ou **📄 Baixar PDF** ao final do expediente para gerar o relatório.

---

**Autor:** Fernando Sato  
**Versão:** 25.0
