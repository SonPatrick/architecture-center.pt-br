---
title: Aprendizado de máquina em escala
description: ''
author: zoinerTejada
ms:date: 02/12/2018
ms.openlocfilehash: a92060008f90f43f71869bd1ad251af150b4a9db
ms.sourcegitcommit: c441fd165e6bebbbbbc19854ec6f3676be9c3b25
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 03/31/2018
---
# <a name="machine-learning-at-scale"></a><span data-ttu-id="91469-102">Aprendizado de máquina em escala</span><span class="sxs-lookup"><span data-stu-id="91469-102">Machine learning at scale</span></span>

<span data-ttu-id="91469-103">O ML (aprendizado de máquina) é uma técnica usada para treinar modelos preditivos com base em algoritmos matemáticos.</span><span class="sxs-lookup"><span data-stu-id="91469-103">Machine learning (ML) is a technique used to train predictive models based on mathematical algorithms.</span></span> <span data-ttu-id="91469-104">O aprendizado de máquina analisa as relações entre os campos de dados para prever valores desconhecidos.</span><span class="sxs-lookup"><span data-stu-id="91469-104">Machine learning analyzes the relationships between data fields to predict unknown values.</span></span>

<span data-ttu-id="91469-105">A criação e implantação de um modelo de aprendizado de máquina é um processo iterativo:</span><span class="sxs-lookup"><span data-stu-id="91469-105">Creating and deploying a machine learning model is an iterative process:</span></span>

* <span data-ttu-id="91469-106">Os cientistas de dados exploram os dados de origem para determinar as relações entre os *recursos* e os *rótulos* previstos.</span><span class="sxs-lookup"><span data-stu-id="91469-106">Data scientists explore the source data to determine relationships between *features* and predicted *labels*.</span></span>
* <span data-ttu-id="91469-107">Os cientistas de dados treinam e validam modelos com base em algoritmos apropriados para encontrar o modelo ideal para previsão.</span><span class="sxs-lookup"><span data-stu-id="91469-107">The data scientists train and validate models based on appropriate algorithms to find the optimal model for prediction.</span></span>
* <span data-ttu-id="91469-108">O modelo ideal é implantado em produção, como um serviço Web ou outra função encapsulada.</span><span class="sxs-lookup"><span data-stu-id="91469-108">The optimal model is deployed into production, as a web service or some other encapsulated function.</span></span>
* <span data-ttu-id="91469-109">Conforme novos dados são coletados, o modelo é periodicamente retreinado para melhorar sua eficácia.</span><span class="sxs-lookup"><span data-stu-id="91469-109">As new data is collected, the model is periodically retrained to improve is effectiveness.</span></span>

<span data-ttu-id="91469-110">O aprendizado de máquina em escala aborda dois interesses de escalabilidade diferentes.</span><span class="sxs-lookup"><span data-stu-id="91469-110">Machine learning at scale addresses two different scalability concerns.</span></span> <span data-ttu-id="91469-111">O primeiro é o treinamento de um modelo em conjuntos grandes de dados que exigem funcionalidades de expansão de um cluster a ser treinado.</span><span class="sxs-lookup"><span data-stu-id="91469-111">The first is training a model against large data sets that require the scale-out capabilities of a cluster to train.</span></span> <span data-ttu-id="91469-112">O segundo concentra-se na operacionalização do modelo aprendido de forma que ele possa ser dimensionado para atender às demandas dos aplicativos que o consomem.</span><span class="sxs-lookup"><span data-stu-id="91469-112">The second centers is operationalizating the learned model in a way that can scale to meet the demands of the applications that consume it.</span></span> <span data-ttu-id="91469-113">Normalmente, isso é feito pela implantação das funcionalidades preditivas como um serviço Web que podem então ser expandidas.</span><span class="sxs-lookup"><span data-stu-id="91469-113">Typically this is accomplished by deploying the predictive capabilities as a web service that can then be scaled out.</span></span>

<span data-ttu-id="91469-114">O aprendizado de máquina em escala traz o benefício de geração de funcionalidades preditivas avançadas, porque modelos melhores normalmente resultam de mais dados.</span><span class="sxs-lookup"><span data-stu-id="91469-114">Machine learning at scale has the benefit that it can produce powerful, predictive capabilities because better models typically result from more data.</span></span> <span data-ttu-id="91469-115">Depois que um modelo é treinado, ele pode ser implantado como um serviço Web de expansão sem monitoração de estado e de alto desempenho.</span><span class="sxs-lookup"><span data-stu-id="91469-115">Once a model is trained, it can be deployed as a stateless, highly-performant, scale-out web service.</span></span> 

## <a name="model-preparation-and-training"></a><span data-ttu-id="91469-116">Preparação de modelo e treinamento</span><span class="sxs-lookup"><span data-stu-id="91469-116">Model preparation and training</span></span>

<span data-ttu-id="91469-117">Durante a fase de preparação de modelo e treinamento, os cientistas de dados exploram os dados de maneira interativa usando linguagens como o Python e o R para:</span><span class="sxs-lookup"><span data-stu-id="91469-117">During the model preparation and training phase, data scientists explore the data interactively using languages like Python and R to:</span></span>

* <span data-ttu-id="91469-118">Extrair amostras de armazenamentos de dados de alto volume.</span><span class="sxs-lookup"><span data-stu-id="91469-118">Extract samples from high volume data stores.</span></span>
* <span data-ttu-id="91469-119">Localizar e tratar exceções, duplicatas e valores ausentes para limpar os dados.</span><span class="sxs-lookup"><span data-stu-id="91469-119">Find and treat outliers, duplicates, and missing values to clean the data.</span></span>
* <span data-ttu-id="91469-120">Determinar correlações e relações nos dados por meio de análise estatística e visualização.</span><span class="sxs-lookup"><span data-stu-id="91469-120">Determine correlations and relationships in the data through statistical analysis and visualization.</span></span>
* <span data-ttu-id="91469-121">Gerar novos recursos calculados que melhoram a previsibilidade de relações estatísticas.</span><span class="sxs-lookup"><span data-stu-id="91469-121">Generate new calculated features that improve the predictiveness of statistical relationships.</span></span>
* <span data-ttu-id="91469-122">Treinar os modelos de ML com base em algoritmos preditivos.</span><span class="sxs-lookup"><span data-stu-id="91469-122">Train ML models based on predictive algorithms.</span></span>
* <span data-ttu-id="91469-123">Validar os modelos treinados usando dados que foram retidos durante o treinamento.</span><span class="sxs-lookup"><span data-stu-id="91469-123">Validate trained models using data that was withheld during training.</span></span>

<span data-ttu-id="91469-124">Para dar suporte a essa fase interativa de análise e modelagem, a plataforma de dados precisa permitir aos cientistas de dados explorar os dados usando uma variedade de ferramentas.</span><span class="sxs-lookup"><span data-stu-id="91469-124">To support this interactive analysis and modeling phase, the data platform must enable data scientists to explore data using a variety of tools.</span></span> <span data-ttu-id="91469-125">Além disso, o treinamento de um modelo de aprendizado de máquina complexo pode exigir uma grande quantidade de processamento intensivo de amplos volumes de dados; portanto, é essencial ter recursos suficientes para a expansão do treinamento do modelo.</span><span class="sxs-lookup"><span data-stu-id="91469-125">Additionally, the training of a complex machine learning model can require a lot of intensive processing of high volumes of data, so sufficient resources for scaling out the model training is essential.</span></span>

## <a name="model-deployment-and-consumption"></a><span data-ttu-id="91469-126">Implantação e consumo de modelo</span><span class="sxs-lookup"><span data-stu-id="91469-126">Model deployment and consumption</span></span>

<span data-ttu-id="91469-127">Quando um modelo está pronto para ser implantado, ele pode ser encapsulado como um serviço Web e implantado na nuvem, em um dispositivo de borda ou em um ambiente empresarial de execução do ML.</span><span class="sxs-lookup"><span data-stu-id="91469-127">When a model is ready to be deployed, it can be encapsulated as a web service and deployed in the cloud, to an edge device, or within an enterprise ML execution environment.</span></span> <span data-ttu-id="91469-128">Esse processo de implantação é conhecido como operacionalização.</span><span class="sxs-lookup"><span data-stu-id="91469-128">This deployment process is referred to as operationalization.</span></span>

## <a name="challenges"></a><span data-ttu-id="91469-129">Desafios</span><span class="sxs-lookup"><span data-stu-id="91469-129">Challenges</span></span>

<span data-ttu-id="91469-130">O aprendizado de máquina em escala apresenta alguns desafios:</span><span class="sxs-lookup"><span data-stu-id="91469-130">Machine learning at scale produces a few challenges:</span></span>

- <span data-ttu-id="91469-131">Normalmente, você precisa de muitos dados para treinar um modelo, especialmente para modelos de aprendizado profundo.</span><span class="sxs-lookup"><span data-stu-id="91469-131">You typically need a lot of data to train a model, especially for deep learning models.</span></span>
- <span data-ttu-id="91469-132">Você precisa preparar esses conjuntos de Big Data antes mesmo de começar a treinar o modelo.</span><span class="sxs-lookup"><span data-stu-id="91469-132">You need to prepare these big data sets before you can even begin training your model.</span></span>
- <span data-ttu-id="91469-133">A fase de treinamento de modelo precisa acessar os armazenamentos de Big Data.</span><span class="sxs-lookup"><span data-stu-id="91469-133">The model training phase must access the big data stores.</span></span> <span data-ttu-id="91469-134">É comum realizar o treinamento de modelo usando o mesmo cluster de Big Data, como o Spark, que é usado para preparação de dados.</span><span class="sxs-lookup"><span data-stu-id="91469-134">It's common to perform the model training using the same big data cluster, such as Spark, that is used for data preparation.</span></span> 
- <span data-ttu-id="91469-135">Para cenários como aprendizado profundo, você precisará não apenas de um cluster que possa fornecer a expansão em CPUs, mas o cluster também precisará consistir em nós habilitados para GPU.</span><span class="sxs-lookup"><span data-stu-id="91469-135">For scenarios such as deep learning, not only will you need a cluster that can provide you scale out on CPUs, but your cluster will need to consist of GPU-enabled nodes.</span></span>

## <a name="machine-learning-at-scale-in-azure"></a><span data-ttu-id="91469-136">Aprendizado de máquina em escala no Azure</span><span class="sxs-lookup"><span data-stu-id="91469-136">Machine learning at scale in Azure</span></span>

<span data-ttu-id="91469-137">Antes de decidir quais serviços de ML serão usados em treinamento e operacionalização, considere se você precisa mesmo treinar um modelo ou se um modelo predefinido pode atender às suas necessidades.</span><span class="sxs-lookup"><span data-stu-id="91469-137">Before deciding which ML services to use in training and operationalization, consider whether you need to train a model at all, or if a prebuilt model can meet your requirements.</span></span> <span data-ttu-id="91469-138">Em muitos casos, o uso de um modelo predefinido é apenas uma questão de chamar um serviço Web ou usar uma biblioteca de ML para carregar um modelo existente.</span><span class="sxs-lookup"><span data-stu-id="91469-138">In many cases, using a prebuilt model is just a matter of calling a web service or using an ML library to load an existing model.</span></span> <span data-ttu-id="91469-139">Algumas opções incluem:</span><span class="sxs-lookup"><span data-stu-id="91469-139">Some options include:</span></span> 

- <span data-ttu-id="91469-140">Usar os serviços Web fornecidos pelos Serviços Cognitivos da Microsoft.</span><span class="sxs-lookup"><span data-stu-id="91469-140">Use the web services provided by Microsoft Cognitive Services.</span></span>
- <span data-ttu-id="91469-141">Usar os modelos de rede neural pré-treinados fornecidos pelo Cognitive Toolkit.</span><span class="sxs-lookup"><span data-stu-id="91469-141">Use the pretrained neural network models provided by Cognitive Toolkit.</span></span>
- <span data-ttu-id="91469-142">Inserir os modelos serializados fornecidos pelo Core ML para aplicativos iOS.</span><span class="sxs-lookup"><span data-stu-id="91469-142">Embed the serialized models provided by Core ML for an iOS apps.</span></span> 

<span data-ttu-id="91469-143">Se um modelo predefinido não se ajusta aos seus dados ou ao seu cenário, outras opções no Azure incluem o Azure Machine Learning, HDInsight com Spark MLlib e MMLSpark, Cognitive Toolkit e SQL Machine Learning Services.</span><span class="sxs-lookup"><span data-stu-id="91469-143">If a prebuilt model does not fit your data or your scenario, options in Azure include Azure Machine Learning, HDInsight with Spark MLlib and MMLSpark, Cognitive Toolkit, and SQL Machine Learning Services.</span></span> <span data-ttu-id="91469-144">Se você decidir usar um modelo personalizado, precisará criar um pipeline que inclui o treinamento e a operacionalização do modelo.</span><span class="sxs-lookup"><span data-stu-id="91469-144">If you decide to use a custom model, you must design a pipeline that includes model training and operationalization.</span></span> 

![Opções de modelo no Azure](./images/machine-learning-model-training-and-deployment.png)

<span data-ttu-id="91469-146">Para obter uma lista das opções de tecnologia de ML no Azure, consulte os seguintes tópicos:</span><span class="sxs-lookup"><span data-stu-id="91469-146">For a list of technology choices for ML in Azure, see the following topics:</span></span>

- [<span data-ttu-id="91469-147">Escolhendo uma tecnologia de serviços cognitivos</span><span class="sxs-lookup"><span data-stu-id="91469-147">Choosing a cognitive services technology</span></span>](../technology-choices/cognitive-services.md)
- [<span data-ttu-id="91469-148">Escolhendo uma tecnologia de aprendizado de máquina</span><span class="sxs-lookup"><span data-stu-id="91469-148">Choosing a machine learning technology</span></span>](../technology-choices/data-science-and-machine-learning.md)
- [<span data-ttu-id="91469-149">Escolhendo uma tecnologia de processamento de idioma natural</span><span class="sxs-lookup"><span data-stu-id="91469-149">Choosing a natural language processing technology</span></span>](../technology-choices/natural-language-processing.md)