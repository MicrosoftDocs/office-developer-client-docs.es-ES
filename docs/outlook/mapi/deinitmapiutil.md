---
title: DeinitMapiUtil
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeinitMapiUtil
api_type:
- HeaderDef
ms.assetid: e0b8dc9c-cc46-4d27-9497-7a55a0bfdff5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: a9654efc34280941cdbc727bce9912a0a39d0fb9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427349"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="b3aa9-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="b3aa9-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="b3aa9-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b3aa9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b3aa9-105">Libera funciones de utilidad llamadas explícitamente por [la función ScInitMapiUtil](scinitmapiutil.md) o implícitamente por [la función MAPIInitialize.](mapiinitialize.md)</span><span class="sxs-lookup"><span data-stu-id="b3aa9-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="b3aa9-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="b3aa9-106">Header file:</span></span>  <br/> |<span data-ttu-id="b3aa9-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="b3aa9-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="b3aa9-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="b3aa9-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="b3aa9-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="b3aa9-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="b3aa9-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="b3aa9-110">Called by:</span></span>  <br/> |<span data-ttu-id="b3aa9-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="b3aa9-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="b3aa9-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="b3aa9-112">Parameters</span></span>

<span data-ttu-id="b3aa9-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b3aa9-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="b3aa9-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="b3aa9-114">Return value</span></span>

<span data-ttu-id="b3aa9-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="b3aa9-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b3aa9-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="b3aa9-116">Remarks</span></span>

<span data-ttu-id="b3aa9-117">Las **funciones de lanzamiento de la función DeinitMapiUtil** inicializadas con [ScInitMapiUtil](scinitmapiutil.md) o [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="b3aa9-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="b3aa9-118">Cuando se complete el uso de las funciones llamadas por **ScInitMapiUtil,** se debe llamar explícitamente **a DeinitMapiUtil** para liberarlas.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="b3aa9-119">Por el contrario, [MAPIUninitialize](mapiuninitialize.md) llama implícitamente **a DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="b3aa9-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

