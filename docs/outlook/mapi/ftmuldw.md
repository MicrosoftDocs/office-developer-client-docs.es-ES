---
title: FtMulDw
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.FtMulDw
api_type:
- COM
ms.assetid: e135ba67-97be-4ce0-a72e-93c49ed7d6e2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: c823a4e3d08d9082a3b5ac5c4bd8169612caa16e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583998"
---
# <a name="ftmuldw"></a><span data-ttu-id="9345d-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="9345d-103">FtMulDw</span></span>

  
  
<span data-ttu-id="9345d-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9345d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9345d-105">Multiplica a un entero de 64 bits sin signo por un entero sin signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9345d-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="9345d-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="9345d-106">Header file:</span></span>  <br/> |<span data-ttu-id="9345d-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="9345d-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="9345d-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="9345d-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="9345d-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="9345d-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="9345d-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="9345d-110">Called by:</span></span>  <br/> |<span data-ttu-id="9345d-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="9345d-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="9345d-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="9345d-112">Parameters</span></span>

 <span data-ttu-id="9345d-113">_Multiplicador_</span><span class="sxs-lookup"><span data-stu-id="9345d-113">_Multiplier_</span></span>
  
> <span data-ttu-id="9345d-114">[entrada] Una palabra doble que contiene el multiplicador de entero sin signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="9345d-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="9345d-115">_Multiplicando_</span><span class="sxs-lookup"><span data-stu-id="9345d-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="9345d-116">[entrada] Una estructura [FILETIME](filetime.md) que contiene el entero sin signo de 64 bits a ser multiplicado por el valor en el parámetro _multiplicador_ .</span><span class="sxs-lookup"><span data-stu-id="9345d-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="9345d-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="9345d-117">Return value</span></span>

<span data-ttu-id="9345d-118">La función **FtMulDw** devuelve una estructura **FILETIME** que contiene el producto de los dos enteros.</span><span class="sxs-lookup"><span data-stu-id="9345d-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="9345d-119">No se modifican los dos parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="9345d-119">The two input parameters remain unchanged.</span></span> 
  

