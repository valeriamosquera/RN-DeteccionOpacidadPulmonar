# Detección de Opacidades Pulmonares en Radiografías de Tórax Frontales
Redes Neuronales - Instituto Tecnológico de Buenos Aires
Trabajo práctico final de Lourdes Hirschson y Valeria Mosquera

El trabajo fue realizado en múltiples notebooks en las que se dividen a grandes rasgos los estadíos del proyecto. El modelo está basado en YOLO v3 con su debida función de costo y fue implementado usando el framework de Darknet. La métrica de evaluación elegida fue la precisión promedio (mean average precision, mAP). Se utiliza el dataset brindado por RSNA para una competencia de Kaggle que comenzó y finalizó en el 2018, disponible en: https://www.kaggle.com/c/rsna-pneumonia-detection-challenge. Se incluyen tres modelos, los cuales presentan pequeñas variaciones entre sí. Durante el desarrollo del trabajo, se implementaron más modelos pero que fueron descartados por las razones que se indican en las notebooks que se incluyen. El modelo al cual se hace referencia como "Darknet256" fue entrenado con imágenes de 256x256 mientras que el de "Darknet1024" fue entrenado con imágenes de 1024x1024. En ambos casos, las imágenes de train fueron divididas en dos subsets: train y validation. Esto fue debido a que se había decidido utilizar la "Late Submission" a la competencia de Kaggle para testear el modelo. Dado que esto no fue posible, se entrenó un tercer modelo con imágenes de 1024x1024, para el cual se dividió el dataset original en tres subsets: train, validation y test.

- Marco teórico y exploración analítica del dataset (EDA): MarcoTeorico_Hirschson_Mosquera.ipynb
- Materiales y métodos: armado de los archivos en el formato necesario para Darknet:  MaterialesYMetodos_Hirschson_Mosquera.ipynb
- Desarrollo: entrenamiento, validación y testeo del modelo y discusión de resultados: 
    - Final:  Darknet1024_Final_Run_NN.ipynb
    - 1024:  Darknet1024_Run_NN.ipynb  
    - 256:  Darknet256_Run_NN.ipynb
