## Projeto DIO - Como criar um modelo de previsão - Seguindo o Tutorial

**Iniciamos um "novo trabalho de ML Automatizado"**
<img width="1928" height="902" alt="image" src="https://github.com/user-attachments/assets/6384cfcf-5fd3-4fa3-b885-786dfb9234e1" />

**Em Configurações básicas:**  
-Nome do trabalho: "voce escolhe  
-Nome do experimento: Selecione "novo"  
-Novo nome do experimento: "voce escolhe"  
-Descrição: "voce escolhe"  
-Marcas: sem  
Avançar  

<img width="1687" height="844" alt="image" src="https://github.com/user-attachments/assets/6a387eff-e02c-4835-a024-d459388da085" />

**Em Tipo de tarefa e dados:**   
-Selecionar tipo de tarefa: Selecione "Regressão"  
-Selecionar os dados: Clique em "Criar" (abrira uma nova pagina)  
<img width="1687" height="865" alt="image" src="https://github.com/user-attachments/assets/99a25268-c0db-45d2-b3a2-e84ed4199dbb" />

**Prencha com as seguinte informaçoes do tutorial:**  
Em Nome: bike-rentals  
Em Descrição: Historic bike rental data  
Em Tipo: Tabela(mltable)
Avançar  
<img width="1909" height="905" alt="image" src="https://github.com/user-attachments/assets/d29d0d44-7f76-4542-8d9d-e518943b4983" />

**Em Fonte de dados**  
-Selecione "De arquivos locais" 
Avançar
<img width="1479" height="870" alt="image" src="https://github.com/user-attachments/assets/4d8c8fd8-43ca-4e3a-b37d-6a6c7d7b449b" />


**Em Tipo de armazenamento de destino**  

-Tipo de armazenamento de dados: Azure Blob Storage  
-Nome: workspaceblobstore

<img width="1484" height="862" alt="image" src="https://github.com/user-attachments/assets/a68819e9-2c5d-457b-85e9-752acbc87b23" />

**Em Seleção de MLTable**  
**Baixe o arquivo deste link: https://aka.ms/bike-rentals**  
Faça o Upload os arquivo da pasta
Avançar

<img width="1487" height="867" alt="image" src="https://github.com/user-attachments/assets/db4d156d-48dd-41bc-82ed-69f4f9b79e6e" />

**Em Examinar**  
-Clique em criar

<img width="1493" height="870" alt="image" src="https://github.com/user-attachments/assets/40703ade-f3ff-4975-a33d-fa53f83fcd83" />

**Em Tipo de tarefa e dados:** 
Selecione a tarefe que acabou de criar e clique em avançar

<img width="1682" height="859" alt="image" src="https://github.com/user-attachments/assets/1ba9853a-5423-46e8-ae26-54d59de0bb8f" />

**Em Configurações de tarefas**  
-Coluna de destino: rentals(integer)

<img width="1687" height="864" alt="image" src="https://github.com/user-attachments/assets/12ed1b7f-b8f5-45fe-a199-05ecc7c078db" />

**Clique em "Exibir definições de configuração adicionais"**  
-Métrica primária: NormalizedRootMeanSquaredError  
-Desmarque as 3 caixas  
-Modelos permitidos: RandomForest e LightGBM  
Salvar

<img width="635" height="870" alt="image" src="https://github.com/user-attachments/assets/4507c166-6d9c-4940-ad17-2152ceb76b1d" />

**Clique em "Limites"**  
Máximo de avaliações: 3  
Máximo de avaliações simultâneas: 3  
Máximo de nós: 3  
Limite de pontuação da métrica: 0.085  
Tempo limite do experimento (minutos): 15  
Tempo limite de iteração (minutos): 15  
**Validar e testar**  
Tipo de validação: Divisão de validação de treinamento  
Validação de percentual de dados: 10  
Dados de teste: nenhum  
Avançar

<img width="1017" height="704" alt="image" src="https://github.com/user-attachments/assets/00719926-d16e-4008-9436-adc1a725d312" />

**Em Computação**  
-Selecione o tipo de computação: Sem servidor  
-Tipo de máquina virtual: CPU  
-Tipo de máquina virtual: Dedicado  
-Tamanho da máquina virtual: Standard_DS3_v2 (4 núcleo(s), 14GB RAM, 28GB de armazenamento) ou escolha qualquer um disponível.
-Número de Instâncias: 1  
Avançar

<img width="1525" height="765" alt="image" src="https://github.com/user-attachments/assets/e0541add-90ef-4465-964e-6c4d25f5f0c6" />

**Em Examinar**  
Clique em "Enviar trabalho de treiamento"  
Aguarde, pode demorar ate 15min para finalizar  

**Apos Concluido, iremos fazer o teste**  
Clique no nome do "Nome do algoritmo"

<img width="1679" height="872" alt="image" src="https://github.com/user-attachments/assets/cb12c222-19fc-4ab5-a971-778c6d832e05" />

**Em Modelo, va em Implantar e Selecione "Terminal em tempo real"**  
<img width="1693" height="869" alt="image" src="https://github.com/user-attachments/assets/576c5ec0-0908-47bd-a096-0447819adb99" />

**Em Implantar**  
-Contagem de instâncias: 3  
-Máquina virtual: Selecione uma atenda os requsitos  
-Ponto de extremidade: Novo  
-Nome do ponto de extremidade: deixe o que estiver  
-Nome da implantação: deixe o que estiver  
-Inferência de coleta de dado: Desabilidado  
-Modelo de Pacote: Desabilidado  
Implantar  
Aguarde, demora entre 5 a 10 min

<img width="558" height="746" alt="image" src="https://github.com/user-attachments/assets/8eaead1b-63a3-4653-b5a7-c07ba1bc1434" />
**OBS: tive problemas com esse passo caso esteja acontecendo algum erro veja esse link (https://learn.microsoft.com/en-us/answers/questions/2129910/resource-provider-(n-a)-isnt-registered-with-subsc)**  

**Apos Concluido, va em Pontos de Extremidade,aba Testar**
<img width="1922" height="907" alt="image" src="https://github.com/user-attachments/assets/6a390ed8-4257-4ea5-a7b0-3aefda5e5249" />

Insira o codigo:  
```
{
  "input_data": {
    "columns": [
      "day",
      "mnth",
      "year",
      "season",
      "holiday",
      "weekday",
      "workingday",
      "weathersit",
      "temp",
      "atemp",
      "hum",
      "windspeed"
    ],
    "index": [0],
    "data": [[1,1,2022,2,0,1,1,2,0.3,0.3,0.3,0.3]]
  }
 }
```
Clique em Teste  

Ira Aparecer um resultado semelhante a esse:  

```
[
  335.45658004339543
]
```

**Apos todo o processo iremos excluir o serviço criado para nao consumir os creditos.**








