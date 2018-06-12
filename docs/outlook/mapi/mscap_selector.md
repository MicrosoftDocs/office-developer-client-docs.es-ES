---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 420b2661e766ecf97a5e9e488e9c18f29cd91329
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818399"
---
# <a name="mscapselector"></a><span data-ttu-id="d1da4-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="d1da4-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="d1da4-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d1da4-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d1da4-105">Especifica las funciones que se devuelven en un almacén.</span><span class="sxs-lookup"><span data-stu-id="d1da4-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="d1da4-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="d1da4-106">Quick info</span></span>

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a><span data-ttu-id="d1da4-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="d1da4-107">Members</span></span>

 <span data-ttu-id="d1da4-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="d1da4-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="d1da4-109">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="d1da4-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="d1da4-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="d1da4-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="d1da4-111">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="d1da4-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="d1da4-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="d1da4-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="d1da4-113">Capacidades de acerca de la compatibilidad de las carpetas en un almacén.</span><span class="sxs-lookup"><span data-stu-id="d1da4-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="d1da4-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="d1da4-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="d1da4-115">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="d1da4-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="d1da4-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="d1da4-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="d1da4-117">Capacidades de acerca de la compatibilidad de las restricciones en un almacén.</span><span class="sxs-lookup"><span data-stu-id="d1da4-117">Capabilities about supporting restrictions on a store.</span></span>
    

