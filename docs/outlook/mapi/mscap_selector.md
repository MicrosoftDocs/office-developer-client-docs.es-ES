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
ms.openlocfilehash: 8c23788d64fe3703c7c46998cade0bd40d2f3dd2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588128"
---
# <a name="mscapselector"></a><span data-ttu-id="8ae7e-103">MSCAP_SELECTOR</span><span class="sxs-lookup"><span data-stu-id="8ae7e-103">MSCAP_SELECTOR</span></span>

  
  
<span data-ttu-id="8ae7e-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8ae7e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8ae7e-105">Especifica las funciones que se devuelven en un almacén.</span><span class="sxs-lookup"><span data-stu-id="8ae7e-105">Specifies the capabilities to return for a store.</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="8ae7e-106">Información rápida</span><span class="sxs-lookup"><span data-stu-id="8ae7e-106">Quick info</span></span>

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

## <a name="members"></a><span data-ttu-id="8ae7e-107">Members</span><span class="sxs-lookup"><span data-stu-id="8ae7e-107">Members</span></span>

 <span data-ttu-id="8ae7e-108">*MSCAP_SEL_RESERVED1*</span><span class="sxs-lookup"><span data-stu-id="8ae7e-108">*MSCAP_SEL_RESERVED1*</span></span> 
  
> <span data-ttu-id="8ae7e-109">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="8ae7e-109">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="8ae7e-110">*MSCAP_SEL_RESERVED2*</span><span class="sxs-lookup"><span data-stu-id="8ae7e-110">*MSCAP_SEL_RESERVED2*</span></span> 
  
> <span data-ttu-id="8ae7e-111">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="8ae7e-111">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="8ae7e-112">*MSCAP_SEL_FOLDER*</span><span class="sxs-lookup"><span data-stu-id="8ae7e-112">*MSCAP_SEL_FOLDER*</span></span> 
  
> <span data-ttu-id="8ae7e-113">Capacidades de acerca de la compatibilidad de las carpetas en un almacén.</span><span class="sxs-lookup"><span data-stu-id="8ae7e-113">Capabilities about supporting folders on a store.</span></span>
    
 <span data-ttu-id="8ae7e-114">*MSCAP_SEL_RESERVED3*</span><span class="sxs-lookup"><span data-stu-id="8ae7e-114">*MSCAP_SEL_RESERVED3*</span></span> 
  
> <span data-ttu-id="8ae7e-115">Este miembro está reservado para el uso interno de Outlook y no se admite.</span><span class="sxs-lookup"><span data-stu-id="8ae7e-115">This member is reserved for the internal use of Outlook and is not supported.</span></span> 
    
 <span data-ttu-id="8ae7e-116">*MSCAP_SEL_RESTRICTION*</span><span class="sxs-lookup"><span data-stu-id="8ae7e-116">*MSCAP_SEL_RESTRICTION*</span></span> 
  
> <span data-ttu-id="8ae7e-117">Capacidades de acerca de la compatibilidad de las restricciones en un almacén.</span><span class="sxs-lookup"><span data-stu-id="8ae7e-117">Capabilities about supporting restrictions on a store.</span></span>
    

