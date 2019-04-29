---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417206"
---
# <a name="mscapselector"></a><span data-ttu-id="1caf5-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="1caf5-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="1caf5-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1caf5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1caf5-105">Especifica las funciones que se van a devolver para un almacén.</span><span class="sxs-lookup"><span data-stu-id="1caf5-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="1caf5-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="1caf5-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="1caf5-107">Miembros</span><span class="sxs-lookup"><span data-stu-id="1caf5-107">Members</span></span>

 <span data-ttu-id="1caf5-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="1caf5-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="1caf5-109">Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1caf5-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="1caf5-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="1caf5-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="1caf5-111">Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1caf5-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="1caf5-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="1caf5-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="1caf5-113">Funcionalidades sobre carpetas auxiliares en un almacén.</span><span class="sxs-lookup"><span data-stu-id="1caf5-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="1caf5-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="1caf5-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="1caf5-115">Este miembro está reservado para uso interno de Outlook y no es compatible.</span><span class="sxs-lookup"><span data-stu-id="1caf5-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="1caf5-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="1caf5-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="1caf5-117">Capacidades para admitir restricciones en un almacén.</span><span class="sxs-lookup"><span data-stu-id="1caf5-117">Capabilities about supporting restrictions on a store.</span></span>
    

