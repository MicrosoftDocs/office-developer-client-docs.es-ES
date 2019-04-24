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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336844"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="542e4-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="542e4-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="542e4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="542e4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="542e4-105">Libera funciones de la utilidad llamadas explícitamente por la función [ScInitMapiUtil](scinitmapiutil.md) o implícitamente mediante la función [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="542e4-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="542e4-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="542e4-106">Header file:</span></span>  <br/> |<span data-ttu-id="542e4-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="542e4-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="542e4-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="542e4-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="542e4-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="542e4-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="542e4-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="542e4-110">Called by:</span></span>  <br/> |<span data-ttu-id="542e4-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="542e4-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="542e4-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="542e4-112">Parameters</span></span>

<span data-ttu-id="542e4-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="542e4-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="542e4-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="542e4-114">Return value</span></span>

<span data-ttu-id="542e4-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="542e4-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="542e4-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="542e4-116">Remarks</span></span>

<span data-ttu-id="542e4-117">La función **DeinitMapiUtil** lanza funciones inicializadas con [ScInitMapiUtil](scinitmapiutil.md) o [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="542e4-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="542e4-118">Cuando se completa el uso de las funciones llamadas por **ScInitMapiUtil** , se debe llamar explícitamente a **DeinitMapiUtil** para liberarlos.</span><span class="sxs-lookup"><span data-stu-id="542e4-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="542e4-119">Por el contrario, [MAPIUninitialize](mapiuninitialize.md) llama implícitamente a **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="542e4-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

