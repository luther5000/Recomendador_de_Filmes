# Recomendador de Filmes
Esse projeto consiste na elaboração de um algoritmo capaz de recomendar filmes através da trilha sonora dos mesmos utilizando técnicas de _machine learning_.

## Equipe
* Lutero Lima Goulart
* Arthur Oliveira Ribeiro
* Luiz Henrique dos Santos Souza


# Dataset
O dataset utilizado foi montado através de _web scapping_ feitos na [Wikipedia](https://www.wikipedia.org/) para coleta de nomes de filmes e no [Sountrack.Net](www.soundtrack.net) para coleta do nome das músicas que compõem a trilha
sonora dos mesmos. Por fim, as informações das músicas (como tonalidade, bpm e outros) foram obtidas através do arquivo `csv` disponibilizado no site [AcousticBrainz](https://acousticbrainz.org/). Toda a 
coleção de informações para montagem do dataset utilizado foi feita em sites que permitem as técnicas utilizadas e o processamento das mesmas por modelos de machine learning na forma como foi realizada. 
É possível ver toda a coleta das informações no arquivo `create_csv.ipynb`.

# Funcionamento
O sistema disposto no arquivo `recommendations.ipynb` lê o arquivo `finalDataset.csv` contendo informações sobres as trilhas sonoras dos filmes descritos em `info_music_dataset/filmesJaUsados.txt` e 
então, através de um autoencoder, seleciona uma das músicas dispostas no `csv` e a compara com todas as outras, apontando então os filmes que possuem alguma música com maior semelhança.
