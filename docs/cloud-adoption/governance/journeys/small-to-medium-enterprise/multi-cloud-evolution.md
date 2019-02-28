---
title: 'CAF: Empresa de pequeno a médio porte – evolução de várias nuvens'
titleSuffix: Microsoft Cloud Adoption Framework for Azure
ms.service: architecture-center
ms.subservice: enterprise-cloud-adoption
ms.custom: governance
ms.date: 02/11/2019
description: Exeplicação de empresa de pequeno a médio porte – evolução de várias nuvens
author: BrianBlanchard
ms.openlocfilehash: a5b09c92acc4e165590b5a35827b88b0ca099bed
ms.sourcegitcommit: 273e690c0cfabbc3822089c7d8bc743ef41d2b6e
ms.translationtype: HT
ms.contentlocale: pt-BR
ms.lasthandoff: 02/08/2019
ms.locfileid: "55900383"
---
# <a name="small-to-medium-enterprise-multi-cloud-evolution"></a><span data-ttu-id="f1b60-103">Empresas de pequeno a médio porte: Evolução de várias nuvens</span><span class="sxs-lookup"><span data-stu-id="f1b60-103">Small-to-medium enterprise: Multi-cloud evolution</span></span>

<span data-ttu-id="f1b60-104">Este artigo desenvolve a narrativa adicionando controles de custo para a adoção de várias nuvens.</span><span class="sxs-lookup"><span data-stu-id="f1b60-104">This article evolves the narrative by adding controls for multi-cloud adoption.</span></span>

## <a name="evolution-of-the-narrative"></a><span data-ttu-id="f1b60-105">Evolução da narrativa</span><span class="sxs-lookup"><span data-stu-id="f1b60-105">Evolution of the narrative</span></span>

<span data-ttu-id="f1b60-106">A Microsoft reconhece que os clientes estão adotando várias nuvens para fins específicos.</span><span class="sxs-lookup"><span data-stu-id="f1b60-106">Microsoft recognizes that customers are adopting multiple clouds for specific purposes.</span></span> <span data-ttu-id="f1b60-107">O cliente fictício nesse percurso não é exceção.</span><span class="sxs-lookup"><span data-stu-id="f1b60-107">The fictional customer in this journey is no exception.</span></span> <span data-ttu-id="f1b60-108">Em paralelo ao percurso de adoção do Azure, o sucesso nos negócios levou à aquisição de uma empresa pequena, mas complementar.</span><span class="sxs-lookup"><span data-stu-id="f1b60-108">In parallel to the Azure adoption journey, the business success has led to the acquisition of a small, but complementary business.</span></span> <span data-ttu-id="f1b60-109">Esse negócio que está sendo executado para todas as suas operações de TI em um provedor de nuvem diferente.</span><span class="sxs-lookup"><span data-stu-id="f1b60-109">That business is running all of their IT operations on a different cloud provider.</span></span>

<span data-ttu-id="f1b60-110">Este artigo descreve como as coisas mudam ao integrar a nova organização.</span><span class="sxs-lookup"><span data-stu-id="f1b60-110">This article describes how things change when integrating the new organization.</span></span> <span data-ttu-id="f1b60-111">Para fins de narrativa, presumimos que essa empresa concluiu cada uma das evoluções de governança delimitadas nessa jornada do cliente.</span><span class="sxs-lookup"><span data-stu-id="f1b60-111">For purposes of the narrative, we assume this company has completed each of the governance evolutions outlined in this customer journey.</span></span>

### <a name="evolution-of-the-current-state"></a><span data-ttu-id="f1b60-112">Evolução do estado atual</span><span class="sxs-lookup"><span data-stu-id="f1b60-112">Evolution of the current state</span></span>

<span data-ttu-id="f1b60-113">Na fase anterior dessa narrativa, a empresa começou a enviar ativamente os aplicativos de produção para a nuvem por meio de pipelines de CI/CD.</span><span class="sxs-lookup"><span data-stu-id="f1b60-113">In the previous phase of this narrative, the company had begun actively pushing production applications to the cloud through CI/CD pipelines.</span></span>

<span data-ttu-id="f1b60-114">Desde então, ocorreram algumas mudanças que afetarão a governança:</span><span class="sxs-lookup"><span data-stu-id="f1b60-114">Since then, some things have changed that will affect governance:</span></span>

- <span data-ttu-id="f1b60-115">A identidade é controlada por uma instância local do Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f1b60-115">Identity is controlled by an on-premises instance of Active Directory.</span></span> <span data-ttu-id="f1b60-116">A identidade híbrida é facilitada por meio da replicação para o Azure Active Directory.</span><span class="sxs-lookup"><span data-stu-id="f1b60-116">Hybrid identity is facilitated through replication to Azure Active Directory.</span></span>
- <span data-ttu-id="f1b60-117">Operações de TI ou operações na nuvem em grande parte são gerenciadas pelo Azure Monitor e relacionados automações.</span><span class="sxs-lookup"><span data-stu-id="f1b60-117">IT Operations or Cloud Operations are largely managed by Azure Monitor and related automations.</span></span>
- <span data-ttu-id="f1b60-118">Recuperação de desastre / continuidade de negócios é controlada pelas instâncias do Azure Vault.</span><span class="sxs-lookup"><span data-stu-id="f1b60-118">Disaster Recovery / Business Continuity is controlled by Azure Vault instances.</span></span>
- <span data-ttu-id="f1b60-119">A Central de Segurança do Azure é usada para monitorar ataques e violações de segurança.</span><span class="sxs-lookup"><span data-stu-id="f1b60-119">Azure Security Center is used to monitor security violations and attacks.</span></span>
- <span data-ttu-id="f1b60-120">A Central de Segurança do Azure e o Azure Monitor são usados para monitorar a governança de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f1b60-120">Azure Security Center and Azure Monitor are both used to monitor governance of the cloud.</span></span>
- <span data-ttu-id="f1b60-121">O Azure Blueprints, Azure Policy e os grupos de gerenciamento do Azure são usados para automatizar a conformidade com a política.</span><span class="sxs-lookup"><span data-stu-id="f1b60-121">Azure Blueprints, Azure Policy, and Azure management groups are used to automate compliance with policy.</span></span>

### <a name="evolution-of-the-future-state"></a><span data-ttu-id="f1b60-122">Evolução do estado futuro</span><span class="sxs-lookup"><span data-stu-id="f1b60-122">Evolution of the future state</span></span>

<span data-ttu-id="f1b60-123">O objetivo é integrar a empresa de aquisição em operações existentes sempre que possível.</span><span class="sxs-lookup"><span data-stu-id="f1b60-123">The goal is to integrate the acquisition company into existing operations wherever possible.</span></span>

## <a name="evolution-of-tangible-risks"></a><span data-ttu-id="f1b60-124">Evolução de riscos tangíveis</span><span class="sxs-lookup"><span data-stu-id="f1b60-124">Evolution of tangible risks</span></span>

<span data-ttu-id="f1b60-125">**Custo de aquisição de negócios**: A aquisição de um novo negócio está prevista para ser lucrativa em aproximadamente cinco anos.</span><span class="sxs-lookup"><span data-stu-id="f1b60-125">**Business acquisition cost**: Acquisition of the new business is slated to be profitable in approximately five years.</span></span> <span data-ttu-id="f1b60-126">Devido à taxa de retorno lenta, o conselho quer controlar os custos de aquisição o máximo possível.</span><span class="sxs-lookup"><span data-stu-id="f1b60-126">Because of the slow rate of return, the board wants to control acquisition costs, as much as possible.</span></span> <span data-ttu-id="f1b60-127">Há um risco de controle de custos e integração técnica conflitantes entre si.</span><span class="sxs-lookup"><span data-stu-id="f1b60-127">There is a risk of cost control and technical integration conflicting with one another.</span></span>

<span data-ttu-id="f1b60-128">Esse risco de negócios pode ser dividido em alguns riscos técnicos:</span><span class="sxs-lookup"><span data-stu-id="f1b60-128">This business risk can be expanded into a few technical risks:</span></span>

- <span data-ttu-id="f1b60-129">A migração para a nuvem pode produzir os custos de aquisição adicionais</span><span class="sxs-lookup"><span data-stu-id="f1b60-129">Cloud migration might produce additional acquisition costs</span></span>
- <span data-ttu-id="f1b60-130">O novo ambiente pode não ser devidamente controlado, o que pode resultar em violações de política.</span><span class="sxs-lookup"><span data-stu-id="f1b60-130">The new environment might not be properly governed which could result in policy violations.</span></span>

## <a name="evolution-of-the-policy-statements"></a><span data-ttu-id="f1b60-131">Evolução das instruções da política</span><span class="sxs-lookup"><span data-stu-id="f1b60-131">Evolution of the policy statements</span></span>

<span data-ttu-id="f1b60-132">As seguintes alterações à política ajudam a reduzir novos riscos e a orientar a implementação.</span><span class="sxs-lookup"><span data-stu-id="f1b60-132">The following changes to policy will help mitigate the new risks and guide implementation.</span></span>

1. <span data-ttu-id="f1b60-133">Todos os ativos em uma nuvem secundária devem ser monitorados por meio do gerenciamento operacional existente e as ferramentas de monitoramento de segurança</span><span class="sxs-lookup"><span data-stu-id="f1b60-133">All assets in a secondary cloud must be monitored through existing operational management and security monitoring tools</span></span>
2. <span data-ttu-id="f1b60-134">Todas as Unidades de Organização devem ser integradas ao provedor de identidade existente</span><span class="sxs-lookup"><span data-stu-id="f1b60-134">All Organization Units must be integrated into the existing identity provider</span></span>
3. <span data-ttu-id="f1b60-135">O provedor de identidade primária deve reger a autenticação aos ativos na nuvem secundária</span><span class="sxs-lookup"><span data-stu-id="f1b60-135">The primary identity provider should govern authentication to assets in the secondary cloud</span></span>

## <a name="evolution-of-the-best-practices"></a><span data-ttu-id="f1b60-136">Evolução das práticas recomendadas</span><span class="sxs-lookup"><span data-stu-id="f1b60-136">Evolution of the best practices</span></span>

<span data-ttu-id="f1b60-137">Esta seção do artigo evoluirá o design MVP de governança para incluir novas políticas do Azure e uma implementação do Gerenciamento de Custos do Azure.</span><span class="sxs-lookup"><span data-stu-id="f1b60-137">This section of the article will evolve the governance MVP design to include new Azure policies and an implementation of Azure Cost Management.</span></span> <span data-ttu-id="f1b60-138">Juntas, essas duas alterações de design atenderão às novas instruções da política corporativa.</span><span class="sxs-lookup"><span data-stu-id="f1b60-138">Together, these two design changes will fulfill the new corporate policy statements.</span></span>

1. <span data-ttu-id="f1b60-139">Conectar as redes.</span><span class="sxs-lookup"><span data-stu-id="f1b60-139">Connect the networks.</span></span> <span data-ttu-id="f1b60-140">Esta etapa é executada pelas equipes de rede e segurança de TI e suporte da equipe de governança de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f1b60-140">This step is executed by the Networking and IT Security teams, and supported by the Cloud Governance team.</span></span> <span data-ttu-id="f1b60-141">Adicionar uma conexão do provedor de MPLS/baseado em linha à nova nuvem irá integrar as redes.</span><span class="sxs-lookup"><span data-stu-id="f1b60-141">Adding a connection from the MPLS/leased-line provider to the new cloud will integrate networks.</span></span> <span data-ttu-id="f1b60-142">Adicionar tabelas de roteamento e configurações de firewall irá controlar o acesso e o tráfego entre os ambientes.</span><span class="sxs-lookup"><span data-stu-id="f1b60-142">Adding routing tables and firewall configurations will control access and traffic between the environments.</span></span>
2. <span data-ttu-id="f1b60-143">Consolidar provedores de identidade.</span><span class="sxs-lookup"><span data-stu-id="f1b60-143">Consolidate identity providers.</span></span> <span data-ttu-id="f1b60-144">Dependendo das cargas de trabalho que estão sendo hospedadas na nuvem secundária, há uma variedade de opções para a consolidação do provedor de identidade.</span><span class="sxs-lookup"><span data-stu-id="f1b60-144">Depending on the workloads being hosted in the secondary cloud, there are a variety of options to identity provider consolidation.</span></span> <span data-ttu-id="f1b60-145">Seguem alguns exemplos:</span><span class="sxs-lookup"><span data-stu-id="f1b60-145">The following are a few examples:</span></span>
    1. <span data-ttu-id="f1b60-146">Para aplicativos que se autenticam usando o OAuth 2, os usuários do Active Directory na nuvem secundária simplesmente podem ser replicados para o locatário existente do Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f1b60-146">For applications that authenticate using OAuth 2, users from Active Directory in the secondary cloud can simply be replicated to the existing Azure AD tenant.</span></span> <span data-ttu-id="f1b60-147">Isso garante que todos os usuários podem ser autenticados no locatário.</span><span class="sxs-lookup"><span data-stu-id="f1b60-147">This ensures all users can be authenticated in the tenant.</span></span>
    2. <span data-ttu-id="f1b60-148">Por outro lado, a federação permite UOs fluam para o Active Directory local, em seguida, para a instância do Active Directory Domain Services.</span><span class="sxs-lookup"><span data-stu-id="f1b60-148">At the other extreme, federation allows OUs to flow into Active Directory on-premises, then into the Azure AD instance.</span></span>
3. <span data-ttu-id="f1b60-149">Adicionar ativos ao Azure Site Recovery.</span><span class="sxs-lookup"><span data-stu-id="f1b60-149">Add assets to Azure Site Recovery.</span></span>
    1. <span data-ttu-id="f1b60-150">O Azure Site Recovery foi projetado desde o início como uma ferramenta híbrida/de várias nuvens.</span><span class="sxs-lookup"><span data-stu-id="f1b60-150">Azure Site Recovery was designed from the beginning as a hybrid/multi-cloud tool.</span></span>
    2. <span data-ttu-id="f1b60-151">As VMs na nuvem secundária poderão ser protegidas pelos mesmos processos do Azure Site Recovery usados para proteger ativos locais.</span><span class="sxs-lookup"><span data-stu-id="f1b60-151">VMs in the secondary cloud might be able to be protected by the same Azure Site Recovery processes used to protect on-premises assets.</span></span>
4. <span data-ttu-id="f1b60-152">Adicionar ativos ao Gerenciamento de Custos do Azure</span><span class="sxs-lookup"><span data-stu-id="f1b60-152">Add assets to Azure Cost Management</span></span>
    1. <span data-ttu-id="f1b60-153">O Gerenciamento de Custos do Azure foi projetado desde o início como uma ferramenta híbrida/de várias nuvens.</span><span class="sxs-lookup"><span data-stu-id="f1b60-153">Azure Cost Management was designed from the beginning as a multi-cloud tool.</span></span>
    2. <span data-ttu-id="f1b60-154">Máquinas virtuais na nuvem secundária podem ser compatíveis com o Gerenciamento de Custos do Azure para alguns provedores de nuvem.</span><span class="sxs-lookup"><span data-stu-id="f1b60-154">Virtual machines in the secondary cloud may be compatible with Azure Cost Management for some cloud providers.</span></span> <span data-ttu-id="f1b60-155">Custos adicionais podem ser aplicados.</span><span class="sxs-lookup"><span data-stu-id="f1b60-155">Additional costs may apply.</span></span>
5. <span data-ttu-id="f1b60-156">Adicione ativos para o Azure Monitor.</span><span class="sxs-lookup"><span data-stu-id="f1b60-156">Add assets to Azure Monitor.</span></span>
    1. <span data-ttu-id="f1b60-157">O Azure Monitor foi projetado como uma ferramenta de nuvem híbrida desde o início.</span><span class="sxs-lookup"><span data-stu-id="f1b60-157">Azure Monitor was designed as a hybrid cloud tool from inception.</span></span>
    2. <span data-ttu-id="f1b60-158">Máquinas virtuais na nuvem secundária podem ser compatíveis com os agentes do Azure Monitor, permitindo que sejam incluídos no Azure Monitor para monitoramento operacional.</span><span class="sxs-lookup"><span data-stu-id="f1b60-158">Virtual machines in the secondary cloud may be compatible with Azure Monitor agents, allowing them to be included in Azure Monitor for operational monitoring.</span></span>
6. <span data-ttu-id="f1b60-159">Ferramentas de imposição de governança:</span><span class="sxs-lookup"><span data-stu-id="f1b60-159">Governance enforcement tools:</span></span>
    1. <span data-ttu-id="f1b60-160">A imposição de governança é específico da nuvem.</span><span class="sxs-lookup"><span data-stu-id="f1b60-160">Governance enforcement is cloud-specific.</span></span>
    2. <span data-ttu-id="f1b60-161">As políticas corporativas estabelecidas no percurso da governança não são específicas da nuvem.</span><span class="sxs-lookup"><span data-stu-id="f1b60-161">The corporate policies established in the governance journey are not cloud-specific.</span></span> <span data-ttu-id="f1b60-162">Embora a implementação possa variar da nuvem para nuvem, as políticas podem ser aplicadas ao provedor secundário.</span><span class="sxs-lookup"><span data-stu-id="f1b60-162">While the implementation may vary from cloud to cloud, the policies can be applied to the secondary provider.</span></span>

<span data-ttu-id="f1b60-163">À medida que aumenta a adoção de várias nuvens, a evolução do design acima continuará a amadurecer.</span><span class="sxs-lookup"><span data-stu-id="f1b60-163">As multi-cloud adoption grows, the design evolution above will continue to mature.</span></span>

## <a name="conclusion"></a><span data-ttu-id="f1b60-164">Conclusão</span><span class="sxs-lookup"><span data-stu-id="f1b60-164">Conclusion</span></span>

<span data-ttu-id="f1b60-165">Esta série de artigos descreveu a evolução das práticas recomendadas de governança, alinhadas às experiências desta empresa fictícia.</span><span class="sxs-lookup"><span data-stu-id="f1b60-165">This series of articles outlined the evolution of governance best practices, aligned with the experiences of this fictional company.</span></span> <span data-ttu-id="f1b60-166">Iniciando pequena, mas com a base certa, a empresa pode se mover rapidamente e ainda assim se aplica a quantidade certa de governança no momento certo.</span><span class="sxs-lookup"><span data-stu-id="f1b60-166">By starting small, but with the right foundation, the company could move quickly and yet still apply the right amount of governance at the right time.</span></span> <span data-ttu-id="f1b60-167">O MVP por si só não protege o cliente.</span><span class="sxs-lookup"><span data-stu-id="f1b60-167">The MVP by itself did not protect the customer.</span></span> <span data-ttu-id="f1b60-168">Em vez disso, criou a base para atenuar o risco e adicionou proteções.</span><span class="sxs-lookup"><span data-stu-id="f1b60-168">Instead, it created the foundation to mitigate risk and add protections.</span></span> <span data-ttu-id="f1b60-169">A partir daí, as camadas de governança foram aplicadas para reduzir os riscos tangíveis.</span><span class="sxs-lookup"><span data-stu-id="f1b60-169">From there, layers of governance were applied to mitigate tangible risks.</span></span> <span data-ttu-id="f1b60-170">O percurso exato apresentado aqui não se alinha 100% com as experiências de qualquer leitor.</span><span class="sxs-lookup"><span data-stu-id="f1b60-170">The exact journey presented here won't align 100% with the experiences of any reader.</span></span> <span data-ttu-id="f1b60-171">Em vez disso, serve como um padrão de governança incremental.</span><span class="sxs-lookup"><span data-stu-id="f1b60-171">Rather, it serves as a pattern for incremental governance.</span></span> <span data-ttu-id="f1b60-172">O leitor é aconselhado a fim de adaptar essas práticas recomendadas de acordo com suas próprias restrições exclusivas e requisitos de governança.</span><span class="sxs-lookup"><span data-stu-id="f1b60-172">The reader is advised to mold these best practices to fit their own unique constraints and governance requirements.</span></span>