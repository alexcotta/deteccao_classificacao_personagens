# Projeto detecção e classificação de personagens

Este projeto aplica redes neurais convolucionais para detectar e classificar
os personagens do seriado NCIS na imagem de entrada usando o modelo ResNet50 e também a biblioteca DeepFace.

## Tecnologias Usadas
- TensorFlow e Keras: Bibliotecas para treinamento e uso de modelos de deep learning.
- ResNet50: Modelo pré-treinado para classificação de imagens.
- DeepFace: Biblioteca para análise facial e criação dos embeddings das faces.
- OpenCV: Biblioteca para processamento de imagens.
- MTCNN: Detecção de faces.
- Matplotlib: Biblioteca para exibição de imagens.

### Requisitos
```bash
pip install tensorflow keras opencv-python-headless matplotlib mtcnn scikit-learn
pip install lz4
pip install deepface
```
### Como usar

1. **Preparar as imagens**

   Cada personagem que deseja detectar e classificar deve ter uma imagem própria para comparação:

   - nick_torres
   - parker
   - knight
   - mgcee
   
2. **Execute o código**

   Após instalação e criação das imagens execute o código:

   ```python
	image_path = './ncis.jpg'  # Substitua pelo caminho da imagem que você deseja analisar

	# Função para detectar e classificar as faces
	classified_image, classifications = detect_faces_and_classify_with_names(image_path)

	# Exibir a imagem com as classificações
	import matplotlib.pyplot as plt
	plt.figure(figsize=(12, 12))
	plt.imshow(classified_image)
	plt.axis("off")
	plt.show()

	# Exibir as classificações no console
	print("Classificações detectadas:")
	for idx, classification in enumerate(classifications):
		print(f"Face {idx + 1}: {classification}")
	```
   

3. **Visualize o resultado**

   A imagem que contem o resultado da detecção e classificação dos personagens encontra-se em:

   ```bash
   /ncis.jpg
   ```
