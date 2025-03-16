### **1. `find`**
- **O que faz**: Procura arquivos e diretórios com base em critérios como nome, tipo, tamanho, data de modificação, etc.
- **Exemplos**:
  ```bash
  # Encontrar todos os arquivos .txt no diretório atual e subdiretórios
  find . -name "*.txt"

  # Encontrar arquivos modificados nos últimos 7 dias
  find . -type f -mtime -7

  # Encontrar arquivos maiores que 1MB
  find . -type f -size +1M
  ```

---

### **2. `grep`**
- **O que faz**: Procura por padrões (texto ou expressões regulares) dentro de arquivos.
- **Exemplos**:
  ```bash
  # Procurar a palavra "error" em um arquivo
  grep "error" arquivo.log

  # Procurar recursivamente em todos os arquivos de um diretório
  grep -r "palavra_chave" /caminho/do/diretorio

  # Ignorar maiúsculas/minúsculas
  grep -i "palavra" arquivo.txt
  ```

---

### **3. `sed`**
- **O que faz**: Edita textos e arquivos em lote, usando expressões regulares.
- **Exemplos**:
  ```bash
  # Substituir "foo" por "bar" em um arquivo
  sed 's/foo/bar/' arquivo.txt

  # Remover linhas em branco
  sed '/^$/d' arquivo.txt

  # Salvar as alterações no arquivo original (com -i)
  sed -i 's/foo/bar/' arquivo.txt
  ```

---

### **4. `awk`**
- **O que faz**: Processa e analisa arquivos de texto, linha por linha, com base em padrões.
- **Exemplos**:
  ```bash
  # Imprimir a primeira coluna de um arquivo CSV
  awk -F',' '{print $1}' arquivo.csv

  # Somar valores da terceira coluna
  awk '{s+=$3} END {print s}' arquivo.txt

  # Filtrar linhas onde a segunda coluna é maior que 100
  awk '$2 > 100' arquivo.txt
  ```

---

### **5. `rsync`**
- **O que faz**: Sincroniza arquivos e diretórios entre locais (local ou remoto), com opções para preservar permissões, links simbólicos, etc.
- **Exemplos**:
  ```bash
  # Sincronizar um diretório local para outro
  rsync -av /origem/ /destino/

  # Sincronizar com um servidor remoto
  rsync -avz /local/ user@remote:/destino/

  # Excluir arquivos específicos durante a sincronização
  rsync -av --exclude='*.tmp' /origem/ /destino/
  ```

---

### **6. `tar`**
- **O que faz**: Compacta e descompacta arquivos no formato `.tar`, muitas vezes combinado com compressão (`.gz`, `.bz2`, etc.).
- **Exemplos**:
  ```bash
  # Compactar um diretório em um arquivo .tar.gz
  tar -czvf arquivo.tar.gz /caminho/do/diretorio

  # Descompactar um arquivo .tar.gz
  tar -xzvf arquivo.tar.gz

  # Listar o conteúdo de um arquivo .tar.gz sem extrair
  tar -tzvf arquivo.tar.gz
  ```

---

### **7. `ln`**
- **O que faz**: Cria links simbólicos (atalhos) ou links físicos para arquivos e diretórios.
- **Exemplos**:
  ```bash
  # Criar um link simbólico
  ln -s /caminho/do/arquivo /caminho/do/link

  # Criar um link físico
  ln /caminho/do/arquivo /caminho/do/link
  ```

---

### **8. `chmod`**
- **O que faz**: Altera as permissões de arquivos e diretórios.
- **Exemplos**:
  ```bash
  # Dar permissão de execução para o dono do arquivo
  chmod u+x arquivo.sh

  # Dar permissão de leitura e escrita para todos
  chmod a+rw arquivo.txt

  # Definir permissões usando notação numérica
  chmod 755 script.sh
  ```

---

### **9. `chown`**
- **O que faz**: Altera o dono e o grupo de arquivos e diretórios.
- **Exemplos**:
  ```bash
  # Mudar o dono de um arquivo
  chown usuario:grupo arquivo.txt

  # Mudar o dono de um diretório e seu conteúdo recursivamente
  chown -R usuario:grupo /caminho/do/diretorio
  ```

---

### **10. `du`**
- **O que faz**: Mostra o uso de espaço em disco por arquivos e diretórios.
- **Exemplos**:
  ```bash
  # Verificar o tamanho de um diretório
  du -sh /caminho/do/diretorio

  # Verificar o tamanho de todos os subdiretórios
  du -h --max-depth=1 /caminho/do/diretorio
  ```

---

### **11. `df`**
- **O que faz**: Mostra o espaço livre e utilizado em sistemas de arquivos montados.
- **Exemplos**:
  ```bash
  # Verificar o espaço em disco em formato legível
  df -h

  # Verificar o espaço em disco de um sistema de arquivos específico
  df -h /dev/sda1
  ```

---

### **12. `mv`**
- **O que faz**: Move ou renomeia arquivos e diretórios.
- **Exemplos**:
  ```bash
  # Mover um arquivo para outro diretório
  mv arquivo.txt /outro/diretorio/

  # Renomear um arquivo
  mv arquivo_antigo.txt arquivo_novo.txt
  ```

---

### **13. `cp`**
- **O que faz**: Copia arquivos e diretórios.
- **Exemplos**:
  ```bash
  # Copiar um arquivo
  cp arquivo.txt /outro/diretorio/

  # Copiar um diretório recursivamente
  cp -r /diretorio_origem/ /diretorio_destino/
  ```

---

### **14. `rm`**
- **O que faz**: Remove arquivos e diretórios.
- **Exemplos**:
  ```bash
  # Remover um arquivo
  rm arquivo.txt

  # Remover um diretório e seu conteúdo recursivamente
  rm -r /caminho/do/diretorio
  ```

---

### **15. `touch`**
- **O que faz**: Cria um arquivo vazio ou atualiza a data de modificação de um arquivo existente.
- **Exemplos**:
  ```bash
  # Criar um arquivo vazio
  touch novo_arquivo.txt

  # Atualizar a data de modificação de um arquivo
  touch arquivo_existente.txt
  ```

---

### **16. `diff`**
- **O que faz**: Compara dois arquivos ou diretórios e mostra as diferenças.
- **Exemplos**:
  ```bash
  # Comparar dois arquivos
  diff arquivo1.txt arquivo2.txt

  # Comparar dois diretórios
  diff -r /diretorio1/ /diretorio2/
  ```

---

### **17. `tee`**
- **O que faz**: Redireciona a saída de um comando para um arquivo e para a tela ao mesmo tempo.
- **Exemplos**:
  ```bash
  # Salvar a saída de um comando em um arquivo e exibir na tela
  ls -l | tee lista_arquivos.txt
  ```

---

### **18. `xargs`**
- **O que faz**: Constrói e executa comandos a partir da entrada padrão.
- **Exemplos**:
  ```bash
  # Remover todos os arquivos .tmp encontrados pelo find
  find . -name "*.tmp" | xargs rm

  # Executar um comando para cada linha de um arquivo
  cat lista.txt | xargs -I {} comando {}
  ```
---

### **18. `rename`**

- **O que faz**: Renomeia arquivos e diretórios a partir da entrada padrão.
- **Exemplos**:
```bash
# Substitui Cache Por Backup
rename 's/Cache/Backup/' *
# Remove Números no final de arquivos
rename 's/[0-9]+$//' *
# Substitui espaços por underscores
rename 's/ /_/g' *
```
