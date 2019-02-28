---
title: 'CAF: Política de linha de base de segurança nativa da nuvem'
titleSuffix: Microsoft Cloud Adoption Framework for Azure
ms.service: architecture-center
ms.subservice: enterprise-cloud-adoption
ms.custom: governance
ms.date: 02/11/2019
description: Política de linha de base de segurança nativa da nuvem
author: BrianBlanchard
ms.openlocfilehash: fc161009f6ce7aa2b775fe6b3b53ff1e1d62a848
ms.sourcegitcommit: 273e690c0cfabbc3822089c7d8bc743ef41d2b6e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55900197"
---
# <a name="cloud-native-security-baseline-policy"></a><span data-ttu-id="dc35d-103">Política de linha de base de segurança nativa da nuvem</span><span class="sxs-lookup"><span data-stu-id="dc35d-103">Cloud-Native Security Baseline policy</span></span>

<span data-ttu-id="dc35d-104">A [Linha de base de segurança](overview.md) é uma das [cinco disciplinas de Governança de nuvem](../governance-disciplines.md).</span><span class="sxs-lookup"><span data-stu-id="dc35d-104">[Security Baseline](overview.md) is one of the [five disciplines of Cloud Governance](../governance-disciplines.md).</span></span> <span data-ttu-id="dc35d-105">Essa disciplina se concentra em tópicos de segurança geral, incluindo a proteção de rede, ativos digitais, dados, etc. Conforme descrito na [guia de política de revisão](../policy-compliance/what-is-a-cloud-policy-review.md), a CAF inclui três níveis de **política de exemplo**: Nativos de nuvem, Enterprise e Conformidade com o princípio de design da nuvem para cada uma das cinco disciplinas.</span><span class="sxs-lookup"><span data-stu-id="dc35d-105">This discipline focuses on general security topics including protection of the network, digital assets, data, etc. As outlined in the [policy review guide](../policy-compliance/what-is-a-cloud-policy-review.md), the CAF includes three levels of **sample policy**: Cloud-Native, Enterprise, and Cloud Design Principle Compliant for each of the five disciplines.</span></span> <span data-ttu-id="dc35d-106">Este artigo discute a Política de exemplo nativo de nuvem para a Disciplina da linha de base de segurança.</span><span class="sxs-lookup"><span data-stu-id="dc35d-106">This article discusses the Cloud-Native Sample Policy for the Security Baseline Discipline.</span></span>

> [!NOTE]
> <span data-ttu-id="dc35d-107">A Microsoft não está em nenhuma posição de ditar política corporativa ou de TI.</span><span class="sxs-lookup"><span data-stu-id="dc35d-107">Microsoft is in no position to dictate corporate or IT policy.</span></span> <span data-ttu-id="dc35d-108">Este artigo destina-se a ajudá-lo a se preparar para uma revisão de política interna.</span><span class="sxs-lookup"><span data-stu-id="dc35d-108">This article is intended to help you prepare for an internal policy review.</span></span> <span data-ttu-id="dc35d-109">Supomos que essa política de exemplo será estendida, validada e testada com a sua política corporativa antes de usá-la.</span><span class="sxs-lookup"><span data-stu-id="dc35d-109">It is assumed that this sample policy will be extended, validated, and tested against your corporate policy before attempting to use it.</span></span> <span data-ttu-id="dc35d-110">Qualquer uso dessa política de exemplo, como está, não é recomendado.</span><span class="sxs-lookup"><span data-stu-id="dc35d-110">Any use of this sample policy, as is, is discouraged.</span></span>

## <a name="policy-alignment"></a><span data-ttu-id="dc35d-111">Alinhamento de políticas</span><span class="sxs-lookup"><span data-stu-id="dc35d-111">Policy alignment</span></span>

<span data-ttu-id="dc35d-112">Essa política de exemplo sintetiza um cenário de nuvem nativa, o que significa que as ferramentas e plataformas fornecidas pelo Azure são suficientes para reduzir os riscos de negócios sobre uma implantação.</span><span class="sxs-lookup"><span data-stu-id="dc35d-112">This sample policy synthesizes a Cloud Native scenario, meaning that the tools and platforms provided by Azure are sufficient to mitigate business risks regarding a deployment.</span></span> <span data-ttu-id="dc35d-113">Nesse cenário, supõe-se que uma configuração simples dos serviços padrão do Azure forneçam proteção suficiente do ativo.</span><span class="sxs-lookup"><span data-stu-id="dc35d-113">In this scenario, it is assumed that a simple configuration of the default Azure services provides sufficient asset protection.</span></span>

## <a name="cloud-security-and-compliance"></a><span data-ttu-id="dc35d-114">Segurança e conformidade de nuvem</span><span class="sxs-lookup"><span data-stu-id="dc35d-114">Cloud security and compliance</span></span>

<span data-ttu-id="dc35d-115">A segurança é integrada em cada aspecto do Azure, oferecendo vantagens de segurança exclusivas derivadas da inteligência de segurança global, controles sofisticados voltados para o cliente e infraestrutura de proteção segura.</span><span class="sxs-lookup"><span data-stu-id="dc35d-115">Security is integrated into every aspect of Azure, offering unique security advantages derived from global security intelligence, sophisticated customer-facing controls, and a secure, hardened infrastructure.</span></span> <span data-ttu-id="dc35d-116">Essa poderosa combinação ajuda a proteger seus aplicativos e dados, dar suporte a seus esforços de conformidade e fornecer segurança econômica para organizações de todos os tamanhos.</span><span class="sxs-lookup"><span data-stu-id="dc35d-116">This powerful combination helps protect your applications and data, support your compliance efforts, and provide cost-effective security for organizations of all sizes.</span></span> <span data-ttu-id="dc35d-117">Essa abordagem cria uma forte posição inicial para qualquer política de segurança, mas não nega a necessidade de práticas de segurança igualmente fortes relacionadas aos serviços de segurança sendo usados.</span><span class="sxs-lookup"><span data-stu-id="dc35d-117">This approach creates a strong starting position for any security policy, but does not negate the need for equally strong security practices related to the security services being used.</span></span>

### <a name="built-in-security-controls"></a><span data-ttu-id="dc35d-118">Controles de segurança interna</span><span class="sxs-lookup"><span data-stu-id="dc35d-118">Built-in security controls</span></span>

<span data-ttu-id="dc35d-119">É difícil de manter uma infraestrutura de segurança forte quando os controles de segurança não são intuitivos e precisam ser configurados separadamente.</span><span class="sxs-lookup"><span data-stu-id="dc35d-119">It’s hard to maintain a strong security infrastructure when security controls are not intuitive and need to be configured separately.</span></span> <span data-ttu-id="dc35d-120">O Azure inclui controles de segurança integrados em uma variedade de serviços que ajudam você a proteger os dados e cargas de trabalho rapidamente e a gerenciar risco entre ambientes híbridos.</span><span class="sxs-lookup"><span data-stu-id="dc35d-120">Azure includes built-in security controls across a variety of services that help you protect data and workloads quickly and manage risk across hybrid environments.</span></span> <span data-ttu-id="dc35d-121">Soluções integradas de parceiros também permitem fazer uma transição fácil das proteções existentes para a nuvem.</span><span class="sxs-lookup"><span data-stu-id="dc35d-121">Integrated partner solutions also let you easily transition existing protections to the cloud.</span></span>

### <a name="cloud-native-identity-policies"></a><span data-ttu-id="dc35d-122">Políticas de identidade Nativos de Nuvem</span><span class="sxs-lookup"><span data-stu-id="dc35d-122">Cloud Native identity policies</span></span>

<span data-ttu-id="dc35d-123">A identidade está se tornando o novo plano de controle de limite para segurança, assumindo a função antes exercida pela perspectiva centrada em rede tradicional.</span><span class="sxs-lookup"><span data-stu-id="dc35d-123">Identity is becoming the new boundary control plane for security, taking over that role from the traditional network-centric perspective.</span></span> <span data-ttu-id="dc35d-124">Os perímetros de rede têm se tornado cada vez mais porosos e a defesa do perímetro não pode ser tão eficiente quanto era antes da evolução de trazer seu próprio dispositivo (BYOD) e aplicativos de nuvem.</span><span class="sxs-lookup"><span data-stu-id="dc35d-124">Network perimeters have become increasingly porous and that perimeter defense cannot be as effective as it was before the evolution of bring your own device (BYOD) and cloud applications.</span></span> <span data-ttu-id="dc35d-125">O gerenciamento de identidade do Azure e o controle de acesso permitem acesso contínuo e seguro a todos os seus aplicativos.</span><span class="sxs-lookup"><span data-stu-id="dc35d-125">Azure identity management and access control enable seamless, secure access to all your applications.</span></span>

<span data-ttu-id="dc35d-126">Uma política de nativo de nuvem de exemplo para identidade entre diretórios locais e de nuvem, pode incluir requisitos semelhante ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="dc35d-126">A sample cloud native policy for identity across cloud and on-premises directories, could include requirements like the following:</span></span>

* <span data-ttu-id="dc35d-127">Acesso autorizado a recursos com controle de acesso baseado em função (RBAC), autenticação multifator (MFA) e logon único (SSO)</span><span class="sxs-lookup"><span data-stu-id="dc35d-127">Authorized access to resources with role-based access control (RBAC), multi-factor authentication (MFA), and single sign-on (SSO)</span></span>
* <span data-ttu-id="dc35d-128">Mitigação rápida de identidades de usuário suspeito de comprometimento</span><span class="sxs-lookup"><span data-stu-id="dc35d-128">Quick mitigation of user identities suspected of compromise</span></span>
* <span data-ttu-id="dc35d-129">Just-in-time (JIT), acesso suficiente concedido em uma base por tarefa para limitar a exposição de credenciais de administrador com muitos privilégios</span><span class="sxs-lookup"><span data-stu-id="dc35d-129">Just-in-time (JIT), just-enough access granted on a task-by-task basis to limit exposure of over-privileged admin credentials</span></span>
* <span data-ttu-id="dc35d-130">Identidade do usuário estendida e acesso às políticas em vários ambientes do Azure Active Directory</span><span class="sxs-lookup"><span data-stu-id="dc35d-130">Extended user identity and access to policies across multiple environments through Azure Active Directory</span></span>

<span data-ttu-id="dc35d-131">Embora seja importante entender a [Linha de Base de Identidade](../identity-baseline/overview.md) no contexto de linha de base de segurança, as [Cinco disciplinas de governança de nuvem](../overview.md) chamam a [Linha de base de identidade](../identity-baseline/overview.md) como sua própria disciplina, separada da Linha de base de segurança.</span><span class="sxs-lookup"><span data-stu-id="dc35d-131">While it is important to understand [Identity Baseline](../identity-baseline/overview.md) in the context of Security Baseline, the [Five Disciplines of Cloud Governance](../overview.md) calls out [Identity Baseline](../identity-baseline/overview.md) as its own discipline, separate from Security Baseline.</span></span>

### <a name="network-access-policies"></a><span data-ttu-id="dc35d-132">Políticas de acesso de rede</span><span class="sxs-lookup"><span data-stu-id="dc35d-132">Network access policies</span></span>

<span data-ttu-id="dc35d-133">O controle de rede inclui configuração, gerenciamento e proteção dos elementos de rede como redes virtuais, balanceamento de carga, DNS e gateways.</span><span class="sxs-lookup"><span data-stu-id="dc35d-133">Network control includes the configuration, management, and securing of network elements such as virtual networking, load balancing, DNS, and gateways.</span></span> <span data-ttu-id="dc35d-134">Os controles fornecem um meio para os serviços se comunicarem e interoperarem.</span><span class="sxs-lookup"><span data-stu-id="dc35d-134">The controls provide a means for services to communicate and interoperate.</span></span> <span data-ttu-id="dc35d-135">O Azure inclui uma infraestrutura de rede robusta e segura para dar suporte a seus requisitos de conectividade de aplicativo e de serviço.</span><span class="sxs-lookup"><span data-stu-id="dc35d-135">Azure includes a robust and secure networking infrastructure to support your application and service connectivity requirements.</span></span> <span data-ttu-id="dc35d-136">A conectividade de rede é possível entre os recursos localizados no Azure, entre os recursos locais e aqueles hospedados no Azure e de origem e destino à Internet e ao Azure.</span><span class="sxs-lookup"><span data-stu-id="dc35d-136">Network connectivity is possible between resources located in Azure, between on-premises and Azure hosted resources, and to and from the internet and Azure.</span></span>

<span data-ttu-id="dc35d-137">Uma política de nativo de nuvem para controles de rede pode incluir requisitos semelhantes ao seguinte:</span><span class="sxs-lookup"><span data-stu-id="dc35d-137">A cloud native policy for network controls may include requirements like the following:</span></span>

* <span data-ttu-id="dc35d-138">Conexões híbridas para recursos locais (embora seja tecnicamente possível no Azure), podem não ser permitidas em uma política de nuvem nativa.</span><span class="sxs-lookup"><span data-stu-id="dc35d-138">Hybrid connections to on-premises resources (While technically possible in Azure), might not be allowed in a Cloud Native policy.</span></span> <span data-ttu-id="dc35d-139">Se uma conexão híbrida se provar necessária, um exemplo de política de segurança corporativa mais robusto seria uma referência mais relevante.</span><span class="sxs-lookup"><span data-stu-id="dc35d-139">Should a hybrid connection prove necessary, a more robust Enterprise Security Policy sample would be a more relevant reference.</span></span>
* <span data-ttu-id="dc35d-140">Os usuários podem estabelecer conexões seguras para e dentro do Azure usando redes virtuais e grupos de segurança de rede.</span><span class="sxs-lookup"><span data-stu-id="dc35d-140">Users can establish secure connections to and within Azure using virtual networks and network security groups.</span></span>
* <span data-ttu-id="dc35d-141">O Firewall do Azure protege os hosts do tráfego de rede mal-intencionados por acesso à porta limitado.</span><span class="sxs-lookup"><span data-stu-id="dc35d-141">Native Windows Azure Firewall protects hosts from malicious network traffic by limited port access.</span></span> <span data-ttu-id="dc35d-142">Um bom exemplo dessa política seria o requisito para bloquear (ou não habilitar) tráfego diretamente para uma VM por RDP - TCP/UDP porta 3389.</span><span class="sxs-lookup"><span data-stu-id="dc35d-142">A good example of this policy would be the requirement to block (or not enable) traffic directly to a VM over RDP - TCP/UDP port 3389.</span></span>
* <span data-ttu-id="dc35d-143">Serviços como o Firewall do Aplicativo Web e a Proteção contra DDoS do Azure protegem aplicativos e garantem a disponibilidade para máquinas virtuais em execução no Azure.</span><span class="sxs-lookup"><span data-stu-id="dc35d-143">Services like Web Application Firewall and Azure DDoS Protection safeguard applications and ensure availability for virtual machines running in Azure.</span></span> <span data-ttu-id="dc35d-144">Esses recursos não devem ser desabilitados ou mal utilizados.</span><span class="sxs-lookup"><span data-stu-id="dc35d-144">These features should not be disabled or misused.</span></span>

### <a name="data-protection"></a><span data-ttu-id="dc35d-145">Proteção de dados</span><span class="sxs-lookup"><span data-stu-id="dc35d-145">Data protection</span></span>

<span data-ttu-id="dc35d-146">Uma das chaves de proteção de dados na nuvem é responsável por possíveis estados em que os dados podem ocorrer e quais controles estão disponíveis para esse estado.</span><span class="sxs-lookup"><span data-stu-id="dc35d-146">One of the keys to data protection in the cloud is accounting for the possible states in which your data may occur, and what controls are available for each state.</span></span> <span data-ttu-id="dc35d-147">Em relação às práticas recomendadas de segurança de dados e criptografia do Azure, as recomendações se concentrarão nos estados de dados a seguir:</span><span class="sxs-lookup"><span data-stu-id="dc35d-147">For the purpose of Azure data security and encryption best practices, recommendations focus on the following data states:</span></span>

* <span data-ttu-id="dc35d-148">Controles de criptografia de dados são criados nos serviços integrados de máquinas virtuais para armazenamento e banco de Dados SQL.</span><span class="sxs-lookup"><span data-stu-id="dc35d-148">Data encryption controls are built into services from virtual machines to storage and SQL Database.</span></span>
* <span data-ttu-id="dc35d-149">Como os dados se movem entre nuvens e clientes, isso pode ser protegido usando protocolos de criptografia padrão do setor.</span><span class="sxs-lookup"><span data-stu-id="dc35d-149">As data moves between clouds and customers, it can be protected using industry-standard encryption protocols.</span></span>
* <span data-ttu-id="dc35d-150">O Azure Key Vault permite aos usuários do Azure proteger e controlar chaves de criptografia e outros segredos usados por aplicativos e serviços de nuvem.</span><span class="sxs-lookup"><span data-stu-id="dc35d-150">Azure Key Vault enables users to safeguard and control cryptographic keys and other secrets used by cloud apps and services.</span></span>
* <span data-ttu-id="dc35d-151">A Proteção de Informações do Azure ajudará a classificar, rotular e proteger seus dados confidenciais em aplicativos.</span><span class="sxs-lookup"><span data-stu-id="dc35d-151">Azure Information Protection will help classify, label, and protect your sensitive data in apps.</span></span>

<span data-ttu-id="dc35d-152">Embora esses recursos sejam criados no Azure, cada um dos itens acima requer configuração e pode aumentar os custos.</span><span class="sxs-lookup"><span data-stu-id="dc35d-152">While these features are built into Azure, each of the above requires configuration and could increase costs.</span></span> <span data-ttu-id="dc35d-153">Alinhamento de cada recurso Nativo de Nuvem com um [estratégia de classificação de dados](../policy-compliance/what-is-data-classification.md) é altamente recomendável.</span><span class="sxs-lookup"><span data-stu-id="dc35d-153">Alignment of each Cloud Native feature with a [data classification strategy](../policy-compliance/what-is-data-classification.md) is highly suggested.</span></span>

### <a name="security-monitoring"></a><span data-ttu-id="dc35d-154">Monitoramento de segurança</span><span class="sxs-lookup"><span data-stu-id="dc35d-154">Security monitoring</span></span>

<span data-ttu-id="dc35d-155">O monitoramento de segurança é uma estratégia proativa que audita os recursos para identificar sistemas que não seguem os padrões ou as melhores práticas organizacionais.</span><span class="sxs-lookup"><span data-stu-id="dc35d-155">Security monitoring is a proactive strategy that audits your resources to identify systems that do not meet organizational standards or best practices.</span></span> <span data-ttu-id="dc35d-156">A Central de Segurança do Azure fornece um gerenciamento de segurança unificado e proteção avançada contra ameaças nas cargas de trabalho de nuvem híbrida.</span><span class="sxs-lookup"><span data-stu-id="dc35d-156">Azure Security Center provides unified Security Baseline and advanced threat protection across hybrid cloud workloads.</span></span> <span data-ttu-id="dc35d-157">Com a Central de Segurança, é possível aplicar políticas de segurança em suas cargas de trabalho, limitar a exposição a ameaças e detectar e responder a ataques, incluindo:</span><span class="sxs-lookup"><span data-stu-id="dc35d-157">With Security Center, you can apply security policies across your workloads, limit your exposure to threats, and detect and respond to attacks, including:</span></span>

* <span data-ttu-id="dc35d-158">Exibição unificada sobre a segurança em todas as suas cargas de trabalho locais e na nuvem com a Central de Segurança do Azure</span><span class="sxs-lookup"><span data-stu-id="dc35d-158">Unified view of security across all on-premises and cloud workloads with Azure Security Center</span></span>
* <span data-ttu-id="dc35d-159">Avaliações contínuas de monitoramento e segurança para garantir a conformidade e corrigir quaisquer vulnerabilidades</span><span class="sxs-lookup"><span data-stu-id="dc35d-159">Continuous monitoring and security assessments to ensure compliance and remediate any vulnerabilities</span></span>
* <span data-ttu-id="dc35d-160">Ferramentas interativas e inteligência contextual contra ameaças</span><span class="sxs-lookup"><span data-stu-id="dc35d-160">Interactive tools and contextual threat intelligence for streamlined investigation</span></span>
* <span data-ttu-id="dc35d-161">Registro em log extensivo e integração com as informações de segurança existentes</span><span class="sxs-lookup"><span data-stu-id="dc35d-161">Extensive logging and integration with existing security information</span></span>

### <a name="extending-cloud-native-policies"></a><span data-ttu-id="dc35d-162">Estender as políticas de nuvem nativa</span><span class="sxs-lookup"><span data-stu-id="dc35d-162">Extending Cloud Native policies</span></span>

<span data-ttu-id="dc35d-163">Usar a nuvem pode reduzir essa carga de segurança.</span><span class="sxs-lookup"><span data-stu-id="dc35d-163">Using the cloud can reduce some of the security burden.</span></span> <span data-ttu-id="dc35d-164">A Microsoft fornece a segurança física para datacenters do Azure e ajuda a proteger a plataforma de nuvem contra ameaças de infraestrutura como um ataque de DDoS.</span><span class="sxs-lookup"><span data-stu-id="dc35d-164">Microsoft provides physical security for Azure datacenters and helps protect the cloud platform against infrastructure threats such as a DDoS attack.</span></span> <span data-ttu-id="dc35d-165">Considerando que a Microsoft tem milhares de especialistas de segurança cibernética trabalhando em segurança todos os dias, os recursos para atenuar ataques cibernéticos são consideráveis.</span><span class="sxs-lookup"><span data-stu-id="dc35d-165">Given that Microsoft has thousands of cybersecurity specialists working on security every day, the resources to mitigate cyberattacks are considerable.</span></span> <span data-ttu-id="dc35d-166">Na verdade, enquanto as organizações estavam preocupadas se a nuvem era segura, a maioria agora compreende que considerando o nível de investimento que fornecedores como a Microsoft fazem em pessoas e infra-estrutura especializada, a nuvem é realmente mais segura do que a maioria dos datacenters locais.</span><span class="sxs-lookup"><span data-stu-id="dc35d-166">In fact, while organizations were once worried about whether the cloud was secure, most now understand that given the level of investment that vendors such as Microsoft make in people and specialized infrastructure, the cloud is actually more secure than most on-premises datacenters.</span></span>

<span data-ttu-id="dc35d-167">Mesmo com esse investimento na linha de base de segurança de nuvem nativa, é recomendável que qualquer política de linha de base de segurança se estenda para as políticas nativas de nuvem padrão.</span><span class="sxs-lookup"><span data-stu-id="dc35d-167">Even with this investment in Cloud Native Security Baseline, it is suggested that any Security Baseline policy extend the default Cloud Native policies.</span></span> <span data-ttu-id="dc35d-168">A seguir estão exemplos de políticas estendidas que devem ser considerados, mesmo em um ambiente nativo de nuvem:</span><span class="sxs-lookup"><span data-stu-id="dc35d-168">The following are examples of extended policies that should be considered, even in a Cloud Native environment:</span></span>

* <span data-ttu-id="dc35d-169">**Proteger VMs**.</span><span class="sxs-lookup"><span data-stu-id="dc35d-169">**Secure VMs**.</span></span> <span data-ttu-id="dc35d-170">A segurança deve ser a prioridade mais alta de cada organização e fazê-lo com eficiência requer várias coisas.</span><span class="sxs-lookup"><span data-stu-id="dc35d-170">Security should be every organization's top priority, and doing it effectively requires several things.</span></span> <span data-ttu-id="dc35d-171">Você deve avaliar o estado da segurança, proteger contra ameaças à segurança e, em seguida, detectar e responder rapidamente às ameaças que ocorrem.</span><span class="sxs-lookup"><span data-stu-id="dc35d-171">You must assess your security state, protect against security threats, and then detect and respond rapidly to threats that occur.</span></span>
* <span data-ttu-id="dc35d-172">**Proteger o conteúdo da VM**.</span><span class="sxs-lookup"><span data-stu-id="dc35d-172">**Protect VM contents**.</span></span> <span data-ttu-id="dc35d-173">Configurar os backups automatizados regulares é essencial para proteger contra erros do usuário.</span><span class="sxs-lookup"><span data-stu-id="dc35d-173">Setting up regular automated backups is essential to protect against user errors.</span></span> <span data-ttu-id="dc35d-174">No entanto, isso não é suficiente. Você também deve verificar se os backups estão protegidos contra ataques cibernéticos e estão disponíveis quando você precisar deles.</span><span class="sxs-lookup"><span data-stu-id="dc35d-174">This isn’t enough, though; you must also make sure that your backups are safe from cyberattacks and are available when you need them.</span></span>
* <span data-ttu-id="dc35d-175">**Monitorar as VMs e aplicativos**.</span><span class="sxs-lookup"><span data-stu-id="dc35d-175">**Monitor VMs and applications**.</span></span> <span data-ttu-id="dc35d-176">Esse padrão abrange várias tarefas, incluindo obter informações sobre a integridade de suas VMs, interações de compreensão entre eles e o estabelecimento de maneiras de monitorar os aplicativos que executam essas VMs.</span><span class="sxs-lookup"><span data-stu-id="dc35d-176">This pattern encompasses several tasks, including getting insight into the health of your VMs, understanding interactions among them, and establishing ways to monitor the applications these VMs run.</span></span> <span data-ttu-id="dc35d-177">Todas essas tarefas são essenciais em manter seus aplicativos em execução o tempo todo.</span><span class="sxs-lookup"><span data-stu-id="dc35d-177">All of these tasks are essential in keeping your applications running around the clock.</span></span>

## <a name="next-steps"></a><span data-ttu-id="dc35d-178">Próximas etapas</span><span class="sxs-lookup"><span data-stu-id="dc35d-178">Next steps</span></span>

<span data-ttu-id="dc35d-179">Agora que você analisou a política de exemplo de linha de base de segurança para soluções de nuvem nativa, retornar para o [guia de política de revisão](../policy-compliance/what-is-a-cloud-policy-review.md) para começar a criar essa amostra para criar suas próprias políticas para a adoção da nuvem.</span><span class="sxs-lookup"><span data-stu-id="dc35d-179">Now that you've reviewed the sample Security Baseline policy for Cloud Native solutions, return to the [policy review guide](../policy-compliance/what-is-a-cloud-policy-review.md) to start building on this sample to create your own policies for cloud adoption.</span></span>

> [!div class="nextstepaction"]
> [<span data-ttu-id="dc35d-180">Crie suas próprias políticas usando o guia da política de revisão</span><span class="sxs-lookup"><span data-stu-id="dc35d-180">Build your own policies using the Policy Review Guide</span></span>](../policy-compliance/what-is-a-cloud-policy-review.md)