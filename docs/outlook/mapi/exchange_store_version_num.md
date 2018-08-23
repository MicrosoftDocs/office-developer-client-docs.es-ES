---
title: EXCHANGE_STORE_VERSION_NUM
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 88950eda-85ae-ad7a-46c6-0e1933d35e04
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 152afd68bea44f3485b2cc566f3f0d2768590704
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594477"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="ff824-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="ff824-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="ff824-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ff824-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ff824-105">Almacena información de versión de Microsoft Exchange Server conectados a cuentas en un perfil de Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="ff824-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="ff824-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="ff824-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="ff824-107">Members</span><span class="sxs-lookup"><span data-stu-id="ff824-107">Members</span></span>

 <span data-ttu-id="ff824-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="ff824-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="ff824-109">Número de versión principal que generalmente se incrementa cuando una versión contiene importantes nuevas características y cambios en la funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="ff824-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="ff824-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="ff824-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="ff824-111">Número de versión secundaria que corresponde a un número específico de versión principal y que generalmente se incrementa cuando una versión contiene nuevas características secundarias o revisiones importantes.</span><span class="sxs-lookup"><span data-stu-id="ff824-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="ff824-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="ff824-112">_wBuild_</span></span>
  
- <span data-ttu-id="ff824-113">Número de compilación principal que corresponde a los números de versión principal y secundaria específica y que generalmente se incrementa en una versión interna que contiene las nuevas características o revisiones.</span><span class="sxs-lookup"><span data-stu-id="ff824-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="ff824-114">Este valor también se incrementa cuando la versión es una bifurcación de código interno principales o hito, como un candidato de versión comercial.</span><span class="sxs-lookup"><span data-stu-id="ff824-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="ff824-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="ff824-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="ff824-116">Número de compilación secundaria que generalmente se incrementa en una versión interna que contiene las nuevas características o corrige correspondiente a una compilación principal específica que indica un hito o una sucursal de código principal.</span><span class="sxs-lookup"><span data-stu-id="ff824-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ff824-117">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="ff824-117">See also</span></span>



[<span data-ttu-id="ff824-118">Información sobre las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="ff824-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="ff824-119">Propiedad canónica PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="ff824-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

