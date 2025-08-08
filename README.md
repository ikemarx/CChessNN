# ♟ **CChessNN**  
**Uma Rede Neural Convolucional para Avaliação de Tabuleiros e Aprendizado de Xadrez**  

CChessNN é uma rede neural convolucional (**CNN**) projetada para aprender a **avaliar posições de xadrez** e, futuramente, **jogar xadrez**.  
Todos os dados de treinamento são extraídos do banco de dados público da [♟ Lichess](https://lichess.org).  

---

## 🚀 **Como começar**  

### **0️⃣ Clonar o repositório**  
Baixe o código-fonte no seu computador:  
```bash
git clone https://github.com/usuario/CChessNN.git
cd CChessNN
```

Se ainda não tiver o **Git** instalado:  
- **Windows**: [⬇️ Baixe aqui](https://git-scm.com/download/win)  
- **Linux (Debian/Ubuntu)**:  
```bash
sudo apt update && sudo apt install git
```

---

### **1️⃣ Instalar o Miniconda** 🐍  
O [Miniconda](https://www.anaconda.com/docs/getting-started/miniconda/install#quickstart-install-instructions) gerencia ambientes virtuais e pacotes de forma leve e eficiente.  

Após instalar, verifique se está funcionando:  
```bash
conda --version
```

---

### **2️⃣ Criar e configurar o ambiente**  

#### 🔹 Criar o ambiente  
```bash
conda create --name cchessnn
conda activate cchessnn
```

#### 🔹 Instalar dependências  

1. **Ferramenta para descompactar dados**  
   - **Windows**: [⬇️ Baixe o PeaZip](https://peazip.github.io/)  
   - **Linux**:  
```bash
sudo apt update && sudo apt install zstd
```

2. **Bibliotecas Python**  
```bash
pip install -r requirements.txt
```

3. **Jupyter Lab** (opcional, mas recomendado)  
```bash
conda install jupyterlab
```

---

### **3️⃣ Baixar e preparar a base de dados** 📂  

#### 📥 Baixar o arquivo  
Substitua `YYYY` e `MM` pelo ano e mês desejados:  
```bash
wget https://database.lichess.org/standard/lichess_db_standard_rated_YYYY-MM.pgn.zst
```

#### 📦 Descompactar  
- **Windows**: clique com o botão direito no `.zst` → **"PeaZip > Extract here"**  
- **Linux**:  
```bash
pzstd -d lichess_db_standard_rated_YYYY-MM.pgn.zst
```

#### 🗑️ Remover arquivo compactado (opcional)  
- **Windows**: delete manualmente.  
- **Linux**:  
```bash
rm lichess_db_standard_rated_YYYY-MM.pgn.zst
```

#### ✏️ Renomear para o formato esperado  
```bash
mv lichess_db_standard_rated_YYYY-MM.pgn input.pgn
```

---

### **4️⃣ Iniciar o Jupyter Lab** 💻  
```bash
jupyter lab
```

---

## ✅ **Pronto para rodar!**  
Agora você pode:  
- 📊 **Explorar notebooks no Jupyter Lab** para visualizar e treinar a rede.  
- ⚡ **Rodar scripts pelo terminal** para processar dados e treinar modelos.  

> 💡 Dica: quanto mais dados você baixar, melhor será o aprendizado da rede — mas verifique se seu disco tem espaço suficiente!  

---
📌 **Licença:** Este projeto é de código aberto. Contribuições são bem-vindas!  
