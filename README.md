# Conversão Manual de Imagem: Colorida → Cinza → Binarizada

Este projeto demonstra a **conversão manual** de uma imagem colorida (RGB) para:
1. **Escala de cinza** (valores de 0 a 255)
2. **Imagem binarizada** (apenas preto = 0 e branco = 255)

A implementação **não utiliza funções prontas de processamento de imagem** (como `cv2.cvtColor()` ou `PIL.Image.convert('L')`). Toda a lógica de transformação é feita **pixel a pixel com código próprio**, respeitando fórmulas padrão da área de visão computacional.

Ideal para estudos em **Google Colab** ou ambientes educacionais onde se deseja entender os fundamentos da manipulação de imagens.

---

## ✨ Funcionalidades

- ✅ Carrega imagem colorida (usando `PIL` apenas para I/O — permitido).
- ✅ Converte para escala de cinza usando a **fórmula de luminância ITU-R BT.601**:  
  `Y = 0.299 * R + 0.587 * G + 0.114 * B`
- ✅ Binariza a imagem com limiar ajustável (`threshold`).
- ✅ Exibe as três versões lado a lado (original, cinza, binária).
- ✅ Código 100% transparente e didático.

---

## 🛠️ Requisitos

- Python 3.x
- Bibliotecas (usadas **apenas para carregar, salvar e visualizar**):
  - `numpy`
  - `Pillow` (PIL)
  - `matplotlib`

> 💡 **Observação**: As bibliotecas são usadas **somente para entrada, saída e visualização**. A **lógica de conversão é inteiramente manual**.

---

## 📂 Estrutura do Código

1. **Carrega imagem** (com `PIL`)
2. **Função manual**: RGB → Escala de cinza (pixel a pixel)
3. **Função manual**: Escala de cinza → Binarizada (com limiar)
4. **Visualização** com `matplotlib`

---

## ▶️ Como usar (no Google Colab)

1. Faça upload de uma imagem (ex: `minha_imagem.jpg`) no Colab.
2. Substitua o caminho no código:

```python
img = Image.open('/content/minha_imagem.jpg')
