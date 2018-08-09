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
ms.openlocfilehash: 861a48464193f357224e33eb0348bc7d5372aa10
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19816890"
---
# <a name="ftmuldw"></a><span data-ttu-id="a463e-103">FtMulDw</span><span class="sxs-lookup"><span data-stu-id="a463e-103">FtMulDw</span></span>

  
  
<span data-ttu-id="a463e-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a463e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a463e-105">Multiplica a un entero de 64 bits sin signo por un entero sin signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a463e-105">Multiplies an unsigned 64-bit integer by an unsigned 32-bit integer.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a463e-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a463e-106">Header file:</span></span>  <br/> |<span data-ttu-id="a463e-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="a463e-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="a463e-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="a463e-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a463e-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a463e-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a463e-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a463e-110">Called by:</span></span>  <br/> |<span data-ttu-id="a463e-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a463e-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
FILETIME FtMulDw(
  DWORD Multiplier,
  FILETIME Multiplicand
);
```

## <a name="parameters"></a><span data-ttu-id="a463e-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a463e-112">Parameters</span></span>

 <span data-ttu-id="a463e-113">_Multiplicador_</span><span class="sxs-lookup"><span data-stu-id="a463e-113">_Multiplier_</span></span>
  
> <span data-ttu-id="a463e-114">[entrada] Una palabra doble que contiene el multiplicador de entero sin signo de 32 bits.</span><span class="sxs-lookup"><span data-stu-id="a463e-114">[in] A double word that contains the unsigned 32-bit integer multiplier.</span></span> 
    
 <span data-ttu-id="a463e-115">_Multiplicando_</span><span class="sxs-lookup"><span data-stu-id="a463e-115">_Multiplicand_</span></span>
  
> <span data-ttu-id="a463e-116">[entrada] Una estructura [FILETIME](filetime.md) que contiene el entero sin signo de 64 bits a ser multiplicado por el valor en el parámetro _multiplicador_ .</span><span class="sxs-lookup"><span data-stu-id="a463e-116">[in] A [FILETIME](filetime.md) structure that contains the unsigned 64-bit integer to be multiplied by the value in the  _Multiplier_ parameter.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="a463e-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a463e-117">Return value</span></span>

<span data-ttu-id="a463e-118">La función **FtMulDw** devuelve una estructura **FILETIME** que contiene el producto de los dos enteros.</span><span class="sxs-lookup"><span data-stu-id="a463e-118">The **FtMulDw** function returns a **FILETIME** structure that contains the product of the two integers.</span></span> <span data-ttu-id="a463e-119">No se modifican los dos parámetros de entrada.</span><span class="sxs-lookup"><span data-stu-id="a463e-119">The two input parameters remain unchanged.</span></span> 
  

