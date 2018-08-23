---
title: FtMulDwDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDwDw
api_type:
- COM
ms.assetid: 8c1a342c-d7ae-4e26-b327-a63cdd3c3ee6
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8002698b1644fb63292b4242d4fb3d784a99a03f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22592027"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="d8889-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="d8889-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="d8889-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d8889-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d8889-105">Un entero sin signo de 32 bits se multiplica por otro.</span><span class="sxs-lookup"><span data-stu-id="d8889-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d8889-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d8889-106">Header file:</span></span>  <br/> |<span data-ttu-id="d8889-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="d8889-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="d8889-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="d8889-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d8889-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d8889-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d8889-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d8889-110">Called by:</span></span>  <br/> |<span data-ttu-id="d8889-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="d8889-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="d8889-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d8889-112">Parameters</span></span>

 <span data-ttu-id="d8889-113">_Multiplicando_</span><span class="sxs-lookup"><span data-stu-id="d8889-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="d8889-114">[entrada] Una palabra doble que contiene el entero sin signo de 32 bits a ser multiplicado por el valor en el parámetro _multiplicador_ .</span><span class="sxs-lookup"><span data-stu-id="d8889-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="d8889-115">_Multiplicador_</span><span class="sxs-lookup"><span data-stu-id="d8889-115">_Multiplier_</span></span>
  
> <span data-ttu-id="d8889-116">[entrada] Una palabra doble que contiene el multiplicador de entero sin signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="d8889-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d8889-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d8889-117">Return value</span></span>

<span data-ttu-id="d8889-118">La función **FtMulDwDw** devuelve una estructura [FILETIME](filetime.md) que contiene el producto de los dos enteros.</span><span class="sxs-lookup"><span data-stu-id="d8889-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="d8889-119">No se modifican los dos parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="d8889-119">The two input parameters remain unchanged.</span></span> 
  

