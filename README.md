# Modelo para detecção de fraudes
Esse projeto utiliza dados sintéticos para entender como funciona a detecção de fraudes em modelos de machine learning.

O foco desse projeto foi testar três modelos de machine learning (LogisticRegression,DecisionTreeClassifier,RandomForestClassifier), analisar seus resultados e chegar a conclusão de qual dos três utilizar. Abaixo está as imagens e coclusões que cheguei.


## Análises📊

Utilizei a regressão logística com os dados desbalanceados, o modelo se mostrou muito enviesado, tendo uma tendência significativa em prever a classe majoritária(dados sem fraude). Isso ocorre pela falta de balanceamento e distribuição dos dados
![Image](https://github.com/user-attachments/assets/d6fe75b1-67dc-45d0-81de-c372903af1c7)

Após o balanceamento, utilizei novamento a regressão logística, o que permitiu uma melhora significativa no modelo. Com as classes balanceadas, com os dados balanceados o modelo teve maior facilidade para detectar as fraudes(classe minoritária)
![Image](https://github.com/user-attachments/assets/3fd484e3-b4dd-4afa-ad55-7157914a6c59)


Visualizando os dados balanceados utilizando o Pandas profilling
![Image](https://github.com/user-attachments/assets/496ae42d-879d-4e41-a19d-cefdc8975254)

Utilizando uma arvore de decisão. O modelo preferiu ser mais conservador preferindo errar clientes não fraudulentos como fraudulentos, do que deixar casos de fraude passar. 
![Image](https://github.com/user-attachments/assets/5ff189dc-13bb-4bc2-91f7-a2668f788a51)

Utilizando random forest. Teve um pequeno aumento nos casos de fraude, mas uma grande redução nos casos falsos positivos (clientes classificados como fraudulentos, mas sendo transações normais). O que para um banco pode significar menos clientes ligando para reclamar de transações classificadas como fraudulentas e menor insatisfação dos clientes.
![Image](https://github.com/user-attachments/assets/5c2e50b0-bc32-4d76-b594-853a7a61b06b)

Após comparar os três modelos, optei por utilizar o Random Forest, pois apresentou um melhor equilíbrio entre os erros, com bom desempenho tanto na identificação de fraudes quanto na redução de falsos positivos.

Após a otimização do random forest, é possível observar uma redução significativa nos falsos positivos e falsos negativos, com ambos caindo pela metade. Isso demonstra que a otimização melhorou a identificação de casos fraudulentos e a prevenção de alarmes falsos ( o que pode causar insatisfação por parte dos clientes). Com a redução dos erros, o modelo se tornou mais eficiente, na identificação de fraude e não classificando clientes como fraudulentos.
![Image](https://github.com/user-attachments/assets/eab19745-df69-481f-901f-00e18b16996c)


Algumas hipóteses para reduzir ainda mais  os casos de fraude:
-Realizar um Captcha ou verificação facial/digital ( em dias/horários fora da rotina)
-Obter a localização do cliente
-Perguntas pessoais


## Tecnologias utilizadas 

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/python/python-original.svg" height=100 width=100/>
Python

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/pandas/pandas-original.svg" height=100 width=100 />
 Pandas
 
<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/scikitlearn/scikitlearn-original.svg" height=100 width=100  />
scikitlearn

<img src="https://cdn.jsdelivr.net/gh/devicons/devicon@latest/icons/numpy/numpy-original-wordmark.svg" height=100 width=100/>
NumPy

