# **CChessNN**  
**Uma Rede Neural Convolucional para Avaliação de Tabuleiros e Aprendizado de Xadrez**  

CChessNN é uma rede neural convolucional (CNN) projetada para aprender a avaliar posições de xadrez e, futuramente, jogar xadrez. Todos os dados de treinamento são extraídos do banco de dados público da [Lichess](https://lichess.org).  

---

## **Como começar**  

### **1. Instale o Miniconda**  
Miniconda é uma versão leve do Anaconda, que gerencia ambientes virtuais e pacotes de forma eficiente.  

1. Instale o Miniconda: [Miniconda quick command line install](https://www.anaconda.com/docs/getting-started/miniconda/install#quickstart-install-instructions)   

2. Após a instalação, abra o terminal (ou Anaconda Prompt no Windows) e confirme que o `conda` está instalado:  
   ```bash
   conda --version
   ```

---

### **2. Preparar o ambiente do projeto**  

#### **Crie um ambiente para a CChessNN**  
1. No terminal, crie um novo ambiente chamado `cchessnn`:  
   ```bash
   conda create --name cchessnn
   ```

2. Ative o ambiente recém-criado:  
     ```bash
     conda activate cchessnn
     ```

#### **Instale as dependências do projeto**  
1. Baixe e instale o **PeaZip** (Windows) ou `zstd` (Linux) para descompactar os arquivos.  
   - **Windows**: Baixe o [PeaZip](https://peazip.github.io/).  
   - **Linux**:  
     ```bash
     sudo apt update && sudo apt install zstd
     ```

2. Navegue até o diretório do projeto e instale os pacotes:  
   ```bash
   pip install -r requirements.txt
   ```

#### **Instale o Jupyter Lab**  
No ambiente ativo, instale o Jupyter Lab para explorar notebooks interativamente:  
```bash
conda install jupyterlab
```

---

### **3. Baixar e preparar a base de dados**  

#### **Baixar o arquivo**  
Substitua `YYYY` pelo ano e `MM` pelo mês desejado e execute:  
```bash
wget https://database.lichess.org/standard/lichess_db_standard_rated_YYYY-MM.pgn.zst
```

#### **Descompactar o arquivo no Windows**  
1. Localize o arquivo `.zst` baixado.  
2. Clique com o botão direito no arquivo e escolha **"PeaZip > Extract here"** ou abra o PeaZip e descompacte o arquivo manualmente.  

#### **Descompactar o arquivo no Linux**  
Execute o comando abaixo para descompactar (substitua `YYYY-MM` pelo ano e mês corretos):  
```bash
pzstd -d lichess_db_standard_rated_YYYY-MM.pgn.zst
```

#### **Limpar arquivos antigos para economizar espaço**  
Depois de descompactar, remova o arquivo compactado:  
- **Windows**: Exclua o arquivo manualmente.  
- **Linux**:  
  ```bash
  rm lichess_db_standard_rated_YYYY-MM.pgn.zst
  ```

#### **Renomear para o formato esperado**  
Renomeie o arquivo descompactado para que o código funcione corretamente sem alterações adicionais:  
```bash
mv lichess_db_standard_rated_YYYY-MM.pgn input.pgn
```

---

### **4. Iniciar o Jupyter Lab**  
Com o ambiente configurado, inicie o Jupyter Lab para explorar e rodar os notebooks do projeto:  
```bash
jupyter lab
```

---

## **Pronto para rodar!**  
Agora o ambiente está configurado, os dados estão prontos e você pode começar a explorar o projeto com o Jupyter Lab ou usar o terminal para executar scripts.
