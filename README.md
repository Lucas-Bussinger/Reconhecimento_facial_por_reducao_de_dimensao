# Redução de dimensionalidade por PCA e Reconhecimento facil SEM USO DE REDES NEURAIS
## Parte 1: Análise
### Pessoas:
O dataset Total possui 38 pessoas, com cada pessoa tendo de 60 a 64 imagens de rosto, em iluminação diferente.
Sample de Faces
<img width="693" height="790" alt="original_faces" src="https://github.com/user-attachments/assets/cc53307d-1737-44ac-8587-018f32706624" />

### Diferenças de iluminação:
<img width="693" height="821" alt="pessoa_1_original" src="https://github.com/user-attachments/assets/d6b592e0-72fd-430a-a705-426aef197608" />

<img width="693" height="821" alt="pessoa_2_original" src="https://github.com/user-attachments/assets/8a669889-ebd3-422e-bb3e-7ebf4c1af194" />

<img width="693" height="821" alt="pessoa_3_original" src="https://github.com/user-attachments/assets/c3f112f3-12f7-4976-b9fb-d6462a9cc03a" />

### Aplicação de PCA por SVD ( Singular Value Decomposition )

#### Faces "Primitivas" | Por SVD sem PCA
<img width="1359" height="1466" alt="Eigen_faces_dataset_original" src="https://github.com/user-attachments/assets/356cac8b-b240-4cad-b57a-ba0f719a9c2a" />

#### Energia das Faces "Primitivas" sem PCA
<img width="1565" height="566" alt="Energia_dataset_original_sem_cutoff" src="https://github.com/user-attachments/assets/e44c6e8d-c5ab-4194-abf6-8207318780d9" />

#### Faces "Primitivas" ( cada face original é uma combinação linear destas faces primitivas ) | por SVD em PCA
<img width="1359" height="1466" alt="eigen_faces_dataset_original_PCA" src="https://github.com/user-attachments/assets/13a33ef4-105a-4031-81bb-62bbc2f909f6" />

#### Energia das Faces "Primitivas" com PCA
<img width="1554" height="566" alt="Energia_dataset_original_PCA" src="https://github.com/user-attachments/assets/baa0c462-87ff-4178-b5b2-1dcc24668e18" />


### Plot de pessoas em Espaço DImensional Reduzido ( 3 dimenões sendo representadas ).

#### Autovetores de maiores 3 Importâncias ( todos os rostos compartilham estas características ):
<img width="984" height="822" alt="reducao_dimensionalidade_dataset_original_1" src="https://github.com/user-attachments/assets/b7f232ba-c236-47d2-8fec-1b46aa59a7dd" />

#### Autovetores de (11ª a 13ª) maiores importâncias ( Diferenças visívies no espaço de amostragem ):
<img width="984" height="822" alt="reducao_dimensionalidade_dataset_original_2" src="https://github.com/user-attachments/assets/8cdfaa04-93e6-4008-a78f-31f83e15e901" />

## Parte 2: Recomnhecimento Facial:

### Sample de Faces Utilizadas para Reconhecimento 
** elas foram retiradas do dataset de "treino"
<img width="1431" height="1465" alt="rostos_sample_para_classificacao" src="https://github.com/user-attachments/assets/fb5cde73-a6de-4e35-a8eb-c97ceee09449" />

### Redução de Dimensionalidade ( todas as faces plotadas )
<img width="949" height="701" alt="reducao_dimensionalidade_previsao" src="https://github.com/user-attachments/assets/28f1010e-197a-4969-a9cc-805c18263f5f" />

#### Faces "Primitivas" do dataset reduzido
<img width="1381" height="1489" alt="egen_faces_dataset_predicao" src="https://github.com/user-attachments/assets/49e9ad48-baa2-492e-8232-644918949053" />

### Acurácia do Reconhecimento Facal de acordo com o número de dimensões Utilizadas ( Algorítimo Utilizado: KNN )
<img width="1190" height="590" alt="acuracia_vs_numero_de_dimensoes utilizadas" src="https://github.com/user-attachments/assets/046ca68d-f900-4c1e-800a-fb4abf11aa3e" />









