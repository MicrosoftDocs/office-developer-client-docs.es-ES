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
ms.openlocfilehash: 54561450e7d91d8a30695dacf508758623547e39
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327982"
---
# <a name="ftmuldwdw"></a><span data-ttu-id="f2efb-103">FtMulDwDw</span><span class="sxs-lookup"><span data-stu-id="f2efb-103">FtMulDwDw</span></span>

  
  
<span data-ttu-id="f2efb-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f2efb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f2efb-105">Multiplica un entero unsigned 32-bit por otro.</span><span class="sxs-lookup"><span data-stu-id="f2efb-105">Multiplies one unsigned 32-bit integer by another.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="f2efb-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="f2efb-106">Header file:</span></span>  <br/> |<span data-ttu-id="f2efb-107">Mapiutil. h</span><span class="sxs-lookup"><span data-stu-id="f2efb-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="f2efb-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="f2efb-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="f2efb-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="f2efb-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="f2efb-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="f2efb-110">Called by:</span></span>  <br/> |<span data-ttu-id="f2efb-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="f2efb-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDwDw(
  DWORD Multiplicand,
  DWORD Multiplier
);
```

## <a name="parameters"></a><span data-ttu-id="f2efb-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="f2efb-112">Parameters</span></span>

 <span data-ttu-id="f2efb-113">_Multiplicand_</span><span class="sxs-lookup"><span data-stu-id="f2efb-113">_Multiplicand_</span></span>
  
> <span data-ttu-id="f2efb-114">a Una palabra doble que contiene el entero de 32 bits sin signo que se va a multiplicar por el valor en el parámetro _multiplicador_ .</span><span class="sxs-lookup"><span data-stu-id="f2efb-114">[in] A double word that contains the unsigned 32-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
 <span data-ttu-id="f2efb-115">_Multiplicador_</span><span class="sxs-lookup"><span data-stu-id="f2efb-115">_Multiplier_</span></span>
  
> <span data-ttu-id="f2efb-116">a Una palabra doble que contiene el multiplicador de enteros de 32 bits sin signo.</span><span class="sxs-lookup"><span data-stu-id="f2efb-116">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f2efb-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="f2efb-117">Return value</span></span>

<span data-ttu-id="f2efb-118">La función **FtMulDwDw** devuelve una estructura [FILETIME](filetime.md) que contiene el producto de los dos enteros.</span><span class="sxs-lookup"><span data-stu-id="f2efb-118">The **FtMulDwDw** function returns a [FILETIME](filetime.md) structure that contains the product of the two integers.</span></span> <span data-ttu-id="f2efb-119">Los dos parámetros de entrada permanecen sin cambios.</span><span class="sxs-lookup"><span data-stu-id="f2efb-119">The two input parameters remain unchanged.</span></span> 
  

