# Projeto Face Detection Mini-System

## Descrição Inicial

Neste projeto se buscou entender os preceitos da captura de imagens e de imagens provenientes de vídeo, além do treinamento de um modelo e o reconhecimento dessas imagens, a partir de um banco de dados. Essa proposta, pode ser utilizada em diversos ramos, desde reconhecimento de face para aplicativos, para segurança em diversos aspectos.

Ao término do projeto, é entregue um mini sistema, com possibilidade de cadastro de nome, matrícula e suas imagens, passsando pelo treinamento do modelo e ao final entregando o reconhecimento desssa pessoa de acordo com os dados antes estabelecidos e da confiança em relação a acurácia do modelo.

Para a criação dessa solução de Visão Computacional foram utilizadas as bibliotecas **OpenCV, Pillow e NumPy**.

A escolha da biblioteca **OpenCV** foi devido a sua capacidade de trabalhar em diversos campos da Visão Computacional, especialmente a Detecção de Faces. Foi explorada a utilização de **Multi-task Cascaded Convolutional Neural Network (MTCNN)**, contudo, apesar de entregar grande precisão, até maior que a OpenCV, a entrega era muito lenta, o que reduzia o impacto do reconhecimento, caso houvesse a necessidade de maior velocidade. Por conta disso, optei pela utilização da OpenCV. Já as bibliotecas **Pillow e NumPy** serviram como base para realização de manipualação, leitura e transformação nas imagens.

## Etapas do Projeto

O projeto foi separado em três: Registro, Treino e Reconhecimento. Num primeiro momento, há a inserção dos dados da pessoa dentro do arquivo labelmap.csv, após isso abre-se a webcam e se cadastram diversas imagens (quantas se quiser e quantos mais ângulos, melhor).

Num segundo momento, Treino, ele abre as imagens, as lê como arrays, separa os dados das imagens e os dados do número de matrícula, e por fim treina o modelo, a partir do algoritmo LBPHFaceRecognizer. 

Por fim, ele lê o modelo e o arquivo labelmap.csv, volta com as imagens da webcam e começa a tentar predizer se, com base nos dados inseridos e treinados, a pessoa que está sendo mostrada é alguém registrado. Se sim, são mostrados os dados e o grau de acurácia.

## Conclusão

Através desse projeto foi possível praticar e implementar conceitos importantes da Visão Computacional e propor uma solução para um problema de segurança, que pode ser utilizada por instituições de segurança ou por empresas que buscam melhores mecanismos para se assegurarem de dados.

Como melhorias futuras, acredito que um menu gráfico, utilizando a biblioteca Tkinter ou outra igual ou superior em termos gráficos, traria uma melhor visualiação desse mini sistema e do link entre as etapas.
