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
ms.openlocfilehash: ae6f7d7066638ef1b149d3e411443384d531184d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816636"
---
# <a name="deinitmapiutil"></a><span data-ttu-id="4c74d-103">DeinitMapiUtil</span><span class="sxs-lookup"><span data-stu-id="4c74d-103">DeinitMapiUtil</span></span>

  
  
<span data-ttu-id="4c74d-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4c74d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4c74d-105">Libera las funciones de utilidad llamadas explícitamente por la función [ScInitMapiUtil](scinitmapiutil.md) o implícitamente por la función [MAPIInitialize](mapiinitialize.md) .</span><span class="sxs-lookup"><span data-stu-id="4c74d-105">Releases utility functions called explicitly by the [ScInitMapiUtil](scinitmapiutil.md) function or implicitly by the [MAPIInitialize](mapiinitialize.md) function.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="4c74d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="4c74d-106">Header file:</span></span>  <br/> |<span data-ttu-id="4c74d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="4c74d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="4c74d-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="4c74d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="4c74d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="4c74d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="4c74d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="4c74d-110">Called by:</span></span>  <br/> |<span data-ttu-id="4c74d-111">Aplicaciones cliente</span><span class="sxs-lookup"><span data-stu-id="4c74d-111">Client applications</span></span>  <br/> |
   
```cpp
VOID DeinitMapiUtil( void );
```

## <a name="parameters"></a><span data-ttu-id="4c74d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="4c74d-112">Parameters</span></span>

<span data-ttu-id="4c74d-113">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4c74d-113">None</span></span> 
  
## <a name="return-value"></a><span data-ttu-id="4c74d-114">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="4c74d-114">Return value</span></span>

<span data-ttu-id="4c74d-115">Ninguno</span><span class="sxs-lookup"><span data-stu-id="4c74d-115">None</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="4c74d-116">Observaciones</span><span class="sxs-lookup"><span data-stu-id="4c74d-116">Remarks</span></span>

<span data-ttu-id="4c74d-117">Las funciones de versión de función de **DeinitMapiUtil** inicializadas con [ScInitMapiUtil](scinitmapiutil.md) o [MAPIInitialize](mapiinitialize.md).</span><span class="sxs-lookup"><span data-stu-id="4c74d-117">The **DeinitMapiUtil** function release functions initialized with [ScInitMapiUtil](scinitmapiutil.md) or [MAPIInitialize](mapiinitialize.md).</span></span> 
  
<span data-ttu-id="4c74d-118">Una vez finalizada la utilización de las funciones llamado por **ScInitMapiUtil** , **DeinitMapiUtil** debe llamarse explícitamente para liberarlos.</span><span class="sxs-lookup"><span data-stu-id="4c74d-118">When use of the functions called by **ScInitMapiUtil** is complete, **DeinitMapiUtil** must be explicitly called to release them.</span></span> <span data-ttu-id="4c74d-119">Por el contrario, [MAPIUninitialize](mapiuninitialize.md) implícitamente llama a **DeinitMapiUtil**.</span><span class="sxs-lookup"><span data-stu-id="4c74d-119">In contrast, [MAPIUninitialize](mapiuninitialize.md) implicitly calls **DeinitMapiUtil**.</span></span> 
  

