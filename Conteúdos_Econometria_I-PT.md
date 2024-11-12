Econometria 1 - Visão Geral

date: "11/11/2024" Class18

Este ficheiro é apenas um guia para o curso de Econometria. Contém os principais tópicos e conceitos abordados durante o curso. Este guia não é suficientemente abrangente para compreender totalmente os conteúdos. Recomenda-se utilizar este ficheiro apenas como complemento aos materiais (livros e aulas) da UC.


keywords: Econometria; Modelos Lineares; Modelos Lineares Generalizados;

# Conteúdos de Econometria 1

## 1 Tipos de dados e estruturas de dados

### 1.1 Estruturas de dados

-   **dados seccionais**: dados recolhidos num único ponto no tempo
-   **dados de séries temporais**: dados recolhidos ao longo do tempo
-   **dados em painel**: dados recolhidos ao longo do tempo e em unidades transversais
-   **dados espaciais**: dados recolhidos no espaço (e.g. dados geográficos)

### 1.2 Transformações de dados

-   **transformação logarítmica**: $ \color{purple}y = \log(x)$
-   **variação percentual**: $\color{purple}\frac{y_t - y_{t-1}}{y_{t-1}}$
-   **diferença**: $\color{purple}y_t - y\_{t-1}$
-   **per capita**: $\color{purple}\frac{y}{pop}$
-   **inverso**: $\color{purple}\frac{1}{y}$
-   **defasagem**: $\color{purple}y\_{t-1}$
-   **quadrado**: $\color{purple}y_{sq}=y^2$

### 1.3 Tipos de dados

-   **contínuos**: e.g. rendimento, idade
-   **discretos**: e.g. número de filhos
-   **binários**: e.g. aprovado ou não aprovado
-   **ordinais**: e.g. nível de educação
-   **nominais**: e.g. nome do país
-   **tempo**: e.g. data, hora
-   **geográficos**: e.g. latitude, longitude

### 1.4 Fontes de dados

-   **dados primários**: dados recolhidos pelo pesquisador
-   **dados secundários**: dados recolhidos por outra pessoa
-   **dados administrativos**: dados recolhidos pelo governo ou outras organizações
-   **big data**: conjuntos de dados grandes e complexos
-   **dados abertos**: dados que estão disponíveis gratuitamente para todos
-   **dados proprietários**: dados que são propriedade de uma empresa ou organização

### 1.5 Variáveis - testes

-   **teste de normalidade**: testa se os dados são distribuídos normalmente; e.g. *histograma*; *teste de Shapiro-Wilk*; *teste de Jarque-Bera*; (assimetria e curtose)
-   **coeficiente de variabilidade**: desvio padrão/média;

## 2 Modelos de regressão linear

### 2.1 Regressão linear simples e regressão linear múltipla
-   **Propósito**: Usado para estimar a relação entre uma variável dependente e uma ou mais variáveis independentes.
-   **Método**: Minimiza a soma do quadrado dos resíduos.
-   **Variável Dependente**: Contínua

-   **Equações**:
                - Regressão simples: $\color{purple}y = \beta_0 + \beta_1 x + u$
                - Regressão múltipla: $\color{purple}y = \beta_0 + \beta_1 x_1 + \beta_2 x_2 + ... + \beta_k x_k + u$
                Onde: $\color{purple}y$ é a variável dependente, $\color{purple}x$ é a variável independente, $\color{purple}\beta_0$ é a interseção, $\color{purple}\beta_1...\beta_k$ são os coeficientes das variáveis independentes, $\color{purple}u$ é o termo de erro.

#### 2.1.1 Pressupostos

-   **normalidade**: os erros são distribuídos normalmente
-   **linearidade**: a relação entre a variável dependente e as variáveis independentes é linear
-   **homoscedasticidade**: variância constante dos erros. e.g. *teste de White*; *teste ARCH*; *teste de Park*...
-   **independência**: as observações são independentes umas das outras. e.g. Sem correlação serial entre os erros.
-   **ausência de multicolinearidade**: as variáveis independentes não são altamente correlacionadas entre si. e.g. *teste VIF*; *matriz de correlação*; *gráfico*; *regressões*...

#### 2.1.2 Ajuste do modelo - qualidade do ajuste

-   **R-quadrado**: a proporção da variância na variável dependente que é explicada pelas variáveis independentes.
-   **R-quadrado ajustado**: uma versão modificada do R-quadrado que ajusta para o número de variáveis independentes no modelo.

#### 2.1.3 Interpretação

-   **Coeficientes**: representam a mudança na variável dependente para uma mudança de uma unidade na variável independente. Depende da escala da variável independente e da especificação do modelo.

#### 2.1.4 Teste de Hipóteses

-   **coeficientes individuais**: testa a significância de cada coeficiente. *teste t*
-   **combinação linear de coeficientes**: testa a significância de uma combinação linear de coeficientes. *teste F*
-   **modelo geral**: testa a significância geral do modelo. *teste F*

#### 2.1.5 Mínimos Quadrados Generalizados - *GLS*

#### 2.1.6 Mínimos Quadrados Ponderados - *WLS*

## 3. Avaliação do modelo

-   **teste F**: significância conjunta das variáveis independentes
-   **teste t**: significância dos coeficientes individuais
-   **R-quadrado/R-quadrado ajustado**: qualidade do ajuste
-   **critérios de informação**: AIC, BIC, HQIC
-   **testes de resíduos**: teste de normalidade (Jarque-Bera), heteroscedasticidade.
-   **testes de estrutura**: teste RESET de Ramsey (especificação incorreta - funcional), teste de Chow (quebra estrutural no modelo), testes CUSUM e CUSUMSQ (estabilidade dos coeficientes)
-   **teste de variável redundante**: teste de razão de verossimilhança
-   **teste de variável omitida**: teste de razão de verossimilhança
-   **teste de multicolinearidade**: VIF, regressões

## 4. Algumas extensões

- Sazonalidade
    - deteção:
        - gráfico
        - regressão
    - tratamento:
        - variáveis dummy sazonais
        - ajuste sazonal - decomposição STL
        - séries homólogas
- Variáveis dummy
    - impulso
    - mudança
    - sazonal

## 5. Modelo de variável dependente limitada (modelo de escolha binária)

-   **Propósito**: Usado para modelar variáveis de resultado binário.
-   **Variável Dependente**: Binária (0 ou 1).

### MPL - modelo de probabilidade linear

-   **método**: Mínimo Quadrados Ordinários
        -   **interpretação**: Os coeficientes representam a mudança na probabilidade da variável dependente para uma mudança de uma unidade na variável independente. **Predizer a probabilidade de sucesso (quando d=1)**
        -   **pressupostos**:
                -   **linearidade**: a relação entre a variável dependente e as variáveis independentes é linear
                -   **homoscedasticidade**
                -   **independência**
                -   **normalidade**
-   **principal limitação**: as probabilidades previstas podem estar fora do intervalo [0,1].
-   **percentagem corretamente prevista**: a proporção de observações que são corretamente previstas pelo modelo (nº de vezes que $y = \hat{y}$)
-   **solução**: usar o modelo logit ou probit.

### Modelo Logit e Probit

-   **método**: *Estimativa de máxima verossimilhança*
-   **pressuposto**: linearidade no logit (log odds) ou probit (z-score)
-   **resultado**: sinal e significância estatística dos coeficientes
-   **interpretação**: efeito parcial na média ou efeito parcial médio
-   **Predizer a probabilidade de sucesso (quando d=1)**

#### Ajuste do modelo

-   **pseudo R-quadrado**: uma medida da qualidade do ajuste do modelo.
-   **teste de razão de verossimilhança**: compara o ajuste do modelo com um modelo nulo (apenas com intercepto).
-   **percentagem corretamente prevista**: a proporção de observações que são corretamente previstas pelo modelo (nº de vezes que d=d_hat)

### Modelo Tobit

-   **método**: *Estimativa de máxima verossimilhança*
-   **definição**: usado quando a variável dependente é censurada ou truncada. e.g. rendimento, preços, índice de felicidade; e.g. *censura*: quando a variável dependente é observada apenas se estiver acima ou abaixo de um certo limite (variáveis fora do limite assumem os valores do limite); e.g. *truncamento*: quando a variável dependente é observada apenas se estiver abaixo ou acima de um certo limite (valores fora do limite são removidos da amostra).

## 6. Modelos espaciais (econometria espacial)

Definição: modelos que consideram as relações espaciais entre as observações.
