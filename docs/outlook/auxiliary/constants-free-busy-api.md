---
title: Constantes (API de libre/ocupado)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: ff756bf1-9395-5e50-4f55-1eb0365a84ed
description: Este tema contiene las definiciones de constantes, los identificadores de clase y los identificadores de interfaz para la API de la información de disponibilidad.
ms.openlocfilehash: ec909d449dc9075959fc9c047457577efd52ec3a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816063"
---
# <a name="constants-freebusy-api"></a><span data-ttu-id="3fbf7-103">Constantes (API de libre/ocupado)</span><span class="sxs-lookup"><span data-stu-id="3fbf7-103">Constants (Free/busy API)</span></span>

<span data-ttu-id="3fbf7-104">Este tema contiene las definiciones de constantes, los identificadores de clase y los identificadores de interfaz para la API de la información de disponibilidad.</span><span class="sxs-lookup"><span data-stu-id="3fbf7-104">This topic contains constant definitions, class identifiers, and interface identifiers for the Free/Busy API.</span></span>
  
## <a name="constants"></a><span data-ttu-id="3fbf7-105">Constantes</span><span class="sxs-lookup"><span data-stu-id="3fbf7-105">Constants</span></span>

|<span data-ttu-id="3fbf7-106">**Constante**</span><span class="sxs-lookup"><span data-stu-id="3fbf7-106">**Constant**</span></span>|<span data-ttu-id="3fbf7-107">**Definición**</span><span class="sxs-lookup"><span data-stu-id="3fbf7-107">**Definition**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3fbf7-108">E_NOTIMPL</span><span class="sxs-lookup"><span data-stu-id="3fbf7-108">E_NOTIMPL</span></span>  <br/> | <span data-ttu-id="3fbf7-109">*Tal como se define en el archivo winerror.h archivo de encabezado de Kit de desarrollo de Software (SDK) de Microsoft Windows.*</span><span class="sxs-lookup"><span data-stu-id="3fbf7-109">*As defined in the Microsoft Windows Software Development Kit (SDK) header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="3fbf7-110">E_OUTOFMEMORY</span><span class="sxs-lookup"><span data-stu-id="3fbf7-110">E_OUTOFMEMORY</span></span>  <br/> | <span data-ttu-id="3fbf7-111">*Tal como se define en el archivo winerror.h archivo de encabezado de Windows SDK.*</span><span class="sxs-lookup"><span data-stu-id="3fbf7-111">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="3fbf7-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="3fbf7-112">S_FALSE</span></span>  <br/> | <span data-ttu-id="3fbf7-113">*Tal como se define en el archivo winerror.h archivo de encabezado de Windows SDK.*</span><span class="sxs-lookup"><span data-stu-id="3fbf7-113">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
|<span data-ttu-id="3fbf7-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="3fbf7-114">S_OK</span></span>  <br/> | <span data-ttu-id="3fbf7-115">*Tal como se define en el archivo winerror.h archivo de encabezado de Windows SDK.*</span><span class="sxs-lookup"><span data-stu-id="3fbf7-115">*As defined in the Windows SDK header file winerror.h.*</span></span>  <br/> |
   
## <a name="interface-identifiers"></a><span data-ttu-id="3fbf7-116">Identificadores de interfaz</span><span class="sxs-lookup"><span data-stu-id="3fbf7-116">Interface identifiers</span></span>

<span data-ttu-id="3fbf7-117">Para los siguientes identificadores de interfaz, se supone la macro DEFINE_GUID definida en el guiddef.h de archivo de encabezado de Windows SDK para asociar el nombre simbólico de GUID a su valor.</span><span class="sxs-lookup"><span data-stu-id="3fbf7-117">For the following interface identifiers, assume the DEFINE_GUID macro defined in the Windows SDK header file guiddef.h to associate the GUID symbolic name with its value.</span></span>
  
<span data-ttu-id="3fbf7-118">{00067064-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="3fbf7-118">//{00067064-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="3fbf7-119">DEFINE_GUID (IID_IEnumFBBlock, 0x00067064, 0 x 0, 0 x 0, 0xc0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 46);</span><span class="sxs-lookup"><span data-stu-id="3fbf7-119">DEFINE_GUID(IID_IEnumFBBlock, 0x00067064, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="3fbf7-120">{00067066-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="3fbf7-120">//{00067066-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="3fbf7-121">DEFINE_GUID (IID_IFreeBusyData, 0x00067066, 0 x 0, 0 x 0, 0xc0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 46);</span><span class="sxs-lookup"><span data-stu-id="3fbf7-121">DEFINE_GUID(IID_IFreeBusyData, 0x00067066, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  
<span data-ttu-id="3fbf7-122">{00067067-0000-0000-C000-000000000046}</span><span class="sxs-lookup"><span data-stu-id="3fbf7-122">//{00067067-0000-0000-C000-000000000046}</span></span>
  
<span data-ttu-id="3fbf7-123">DEFINE_GUID (IID_IFreeBusySupport, 0x00067067, 0 x 0, 0 x 0, 0xc0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 0, 0 x 46);</span><span class="sxs-lookup"><span data-stu-id="3fbf7-123">DEFINE_GUID(IID_IFreeBusySupport, 0x00067067, 0x0, 0x0, 0xc0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x0, 0x46);</span></span>
  

