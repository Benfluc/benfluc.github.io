# ANÁLISE PREDITIVA DA DINÂMICA LOGÍSTICA DO CAFÉ NO BRASIL POR MEIO DE MODELOS GRAVITACIONAIS E REDES NEURAIS DO TIPO MLP

 
## Resumo
O presente trabalho avalia a capacidade preditiva do Modelo Gravitacional (MG) e de uma Rede Neural Artificial (RNA) do tipo Multi Layer Perceptron (MLP) na estimativa dos fluxos de transporte de café dos municípios brasileiros para portos e aeroportos de exportação. A metodologia envolveu a extração de dados públicos de exportação do Ministério do Desenvolvimento, Indústria, Comércio e Serviços (MDIC), o cálculo de variáveis explicativas como produção, destino, distância e valor Free on Board (FOB), além da criação de variáveis numéricas a partir de variáveis categóricas que representam características logísticas. Os modelos foram treinados e avaliados utilizando métricas como coeficiente de determinação (R²) e erro absoluto médio (MAE) avaliando seu resultado com e sem as variáveis categóricas. Os resultados demonstram que a rede MLP supera o MG em desempenho preditivo. A inclusão de variáveis categóricas também contribuiu positivamente para a acurácia dos modelos, indicando assim o potencial das redes neurais como ferramentas eficazes na gestão da logística do agronegócio brasileiro.

## Tecnologias
Python, Pandas, Scikit-learn, TensorFlow, MatLab.

## Resultados
- R² > 0.8543
- MAE ~ 0,9101
- Avaliação da inserção de variáveis categóricas nos resultados;
- Comparativo crítico entre a MLP e Modelo Gravitacional.


## Link para o artigo
- [Artigo completo (EN)](https://medium.com/@luciojuniobenfica2/predictive-analysis-of-the-logistics-dynamics-of-coffee-in-brazil-using-gravitational-models-and-746a3ac0d697))
- [Artigo completo (PT)](artigo_previsaoMG.md)

## Códigos
- [Modelo Gravitacional](https://github.com/Benfluc/benfluc.github.io/blob/main/projects/Previsao/Modelo_final.ipynb)
- [MLP](https://github.com/Benfluc/benfluc.github.io/blob/main/projects/Previsao/MG%20e%20MLP.ipynb)
