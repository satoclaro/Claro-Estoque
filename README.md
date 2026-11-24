# Claro - Controle de Equipamentos Diário (Versão 29.0)

Aplicação web responsiva e 100% client-side (offline-first via `localStorage`) em **tema escuro**, desenvolvida para registro, conferência, rastreio de reversa, backup e exportação diária de equipamentos de telecomunicações em campo.

---

## Principais Funcionalidades

- **Cadastro Rápido de Equipamentos**:
  - **Número do Contrato / OS**: Cola automaticamente o número da área de transferência ao clicar/tocar no campo.
  - **Destino / Movimentação**: **Cliente** (Instalação / Entrega) ou **Reversa** (Retirada / Devolução).
  - **Tipo de Equipamento**: `ONT (GPon)`, `EMTA (HFC)`, `Decoder TV 4K / HD`, `Smartcard`, `Chip / ICCID Movel` e `Mesh Wi-Fi`.
  - **Reconhecimento Automático**: Identifica e seleciona automaticamente o tipo de equipamento no menu ao escanear, digitar ou colar o código.
- **Leitor Híbrido com Linha de Mira (Código de Barras + OCR)**:
  - Combina `BarcodeDetector` nativo, `html5-qrcode` (ZXing) e `Tesseract.js` (OCR) operando apenas sobre a área da linha vermelha de mira.
  - **Filtro Inteligente de Etiquetas**: Aceita automaticamente `CM MAC`, `CA ID` / `CAID`, `Smartcard`, `ONT (GPon)` e `ICCID`, rejeitando códigos indesejados como `BOX S/N`, `S/N`, `Serial`, `EAN`, `WIFI 2G/5G MAC`, `EMTA MAC`, `MoCA MAC` e `MAC Ethernet`.
  - **Botão `🔓 Forçar Leitura`**: Captura e copia imediatamente qualquer código de barras ou texto na mira (em 0°, 90° ou 270°), ignorando todos os filtros de rejeição quando necessário.
  - **Controles de Câmera**: `📸 Ler Mira Agora`, `🔓 Forçar Leitura`, `🎯 Focar`, `🔦 Luz` (lanterna) e toque direto na tela da câmera para focar e capturar.
- **Controle de Reversa e Pesquisa**:
  - Marcação de entrega de reversa (`📅 Entregue`) com registro automático de data e hora (`✓ Entregue: DD/MM/AAAA HH:MM`).
  - Busca instantânea por MAC, CA ID, Contrato/OS ou Data.
- **Exportação, Backup e Restauração de Dados**:
  - **Excel (CSV)**, **PDF**, **Exportar JSON (`💾 Exportar JSON`)** e **Importar JSON (`📂 Importar JSON`)**.

---

**Autor:** Fernando Sato  
**Versão:** 29.0 (24/11/2026 20:37)
