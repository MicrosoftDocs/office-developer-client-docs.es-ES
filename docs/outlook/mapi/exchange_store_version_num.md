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
ms.openlocfilehash: bf60b12a6e4575d3504a112aa2b54fb8c4ae23c7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433727"
---
# <a name="exchangestoreversionnum"></a><span data-ttu-id="7b952-103">EXCHANGE_STORE_VERSION_NUM</span><span class="sxs-lookup"><span data-stu-id="7b952-103">EXCHANGE_STORE_VERSION_NUM</span></span>

  
  
<span data-ttu-id="7b952-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7b952-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7b952-105">Almacena la información de versión del servidor de Microsoft Exchange al que están conectadas las cuentas de un perfil de Microsoft Office Outlook.</span><span class="sxs-lookup"><span data-stu-id="7b952-105">Stores version information for the Microsoft Exchange Server that accounts in a Microsoft Office Outlook profile are connected to.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="7b952-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="7b952-106">Quick info</span></span>

```cpp
typedef struct { 
    WORD wMajorVersion; 
    WORD wMinorVersion; 
    WORD wBuild; 
    WORD wMinorBuild; 
} EXCHANGE_STORE_VERSION_NUM; 

```

## <a name="members"></a><span data-ttu-id="7b952-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="7b952-107">Members</span></span>

 <span data-ttu-id="7b952-108">_wMajorVersion_</span><span class="sxs-lookup"><span data-stu-id="7b952-108">_wMajorVersion_</span></span>
  
- <span data-ttu-id="7b952-109">Número de versión principal que se suele incrementar cuando una versión contiene nuevas características importantes y cambios de funcionalidad.</span><span class="sxs-lookup"><span data-stu-id="7b952-109">Major version number that is generally incremented when a release contains significant new features and changes in functionality.</span></span>
    
 <span data-ttu-id="7b952-110">_wMinorVersion_</span><span class="sxs-lookup"><span data-stu-id="7b952-110">_wMinorVersion_</span></span>
  
- <span data-ttu-id="7b952-111">Número de versión secundaria que corresponde a un número de versión principal específico y que, por lo general, se incrementa cuando una versión contiene nuevas características secundarias o correcciones significativas.</span><span class="sxs-lookup"><span data-stu-id="7b952-111">Minor version number that corresponds to a specific major version number and that is generally incremented when a release contains minor new features or significant fixes.</span></span>
    
 <span data-ttu-id="7b952-112">_wBuild_</span><span class="sxs-lookup"><span data-stu-id="7b952-112">_wBuild_</span></span>
  
- <span data-ttu-id="7b952-113">Número de compilación principal que corresponde a números de versiones principales y secundarias específicas y que, por lo general, se incrementa en una versión interna que contiene nuevas características o correcciones.</span><span class="sxs-lookup"><span data-stu-id="7b952-113">Major build number that corresponds to specific major and minor version numbers and that is generally incremented in an internal release that contains new features or fixes.</span></span> <span data-ttu-id="7b952-114">Este valor también se incrementa cuando el lanzamiento es una bifurcación de código interno principal o un hito como, por ejemplo, Release Candidate.</span><span class="sxs-lookup"><span data-stu-id="7b952-114">This value is also incremented when the release is a major internal code branch or milestone, such as a release candidate.</span></span>
    
 <span data-ttu-id="7b952-115">_wMinorBuild_</span><span class="sxs-lookup"><span data-stu-id="7b952-115">_wMinorBuild_</span></span>
  
- <span data-ttu-id="7b952-116">Número de compilación secundaria que suele incrementarse en una versión interna que contiene nuevas características o revisiones correspondientes a una compilación principal específica que denota una bifurcación de código principal o un hito.</span><span class="sxs-lookup"><span data-stu-id="7b952-116">Minor build number that is generally incremented in an internal release that contains new features or fixes corresponding to a specific major build that denotes a major code branch or milestone.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="7b952-117">Vea también</span><span class="sxs-lookup"><span data-stu-id="7b952-117">See also</span></span>



[<span data-ttu-id="7b952-118">Acerca de las adiciones de MAPI</span><span class="sxs-lookup"><span data-stu-id="7b952-118">About MAPI Additions</span></span>](about-mapi-additions.md)
  
[<span data-ttu-id="7b952-119">Propiedad canónica PidTagProfileServerFullVersion</span><span class="sxs-lookup"><span data-stu-id="7b952-119">PidTagProfileServerFullVersion Canonical Property</span></span>](pidtagprofileserverfullversion-canonical-property.md)

