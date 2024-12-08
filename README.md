# **CChessNN**  
**Uma Rede Neural Convolucional para Avaliação de Tabuleiros e Aprendizado de Xadrez**  

CChessNN é uma rede neural convolucional (CNN) projetada para aprender a avaliar posições de xadrez e, futuramente, jogar xadrez. Todos os dados de treinamento são extraídos do banco de dados público da [Lichess](https://lichess.org).  

---

## **Como começar**  

### **1. Clonar o repositório**  
Execute o comando abaixo para clonar este repositório:  
```bash
git clone https://github.com/ikemarx/CChessNN.git
cd CChessNN
```

---

### **2. Preparar o ambiente**

#### **Windows**  
1. **Baixe e instale o [PeaZip](https://peazip.github.io/).**  
   - Após instalar, você poderá usar a interface gráfica para descompactar os arquivos no formato `.zst`.

2. **Baixe e instale o Python:**  
   - Baixe o instalador do [site oficial do Python](https://www.python.org/).  
   - Durante a instalação, marque a opção **"Add Python to PATH"** para configurar o Python no terminal automaticamente.

3. **Instale os pacotes necessários:**  
   - Abra o terminal ou prompt de comando (pressione `Win + R`, digite `cmd` e pressione Enter).  
   - Navegue até a pasta do projeto e instale os pacotes com:  
     ```bash
     pip install -r requirements.txt
     ```

#### **Linux**  
1. Instale o `zstd` diretamente pelo gerenciador de pacotes:  
   ```bash
   sudo apt update && sudo apt install zstd
   ```

2. Instale o Python (caso ainda não esteja instalado) e os pacotes necessários:  
   ```bash
   sudo apt install python3 python3-pip
   pip install -r requirements.txt
   ```

---

### **3. Baixar e preparar a base de dados**  
Os jogos necessários para treinar a rede são extraídos do banco de dados público da Lichess. Siga as instruções abaixo:  

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

## **Pronto para rodar!**  
Agora o ambiente está configurado e os dados estão prontos. Você pode começar a explorar o projeto.  
