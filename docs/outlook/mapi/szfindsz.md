---
title: SzFindSz
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindSz
api_type:
- COM
ms.assetid: f4584569-1246-4ac9-a404-48284e4920d7
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 0cc8f25271d1494ebdaca82caa2e77839f299276
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820832"
---
# <a name="szfindsz"></a><span data-ttu-id="97fb1-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="97fb1-103">SzFindSz</span></span>

  
  
<span data-ttu-id="97fb1-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="97fb1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="97fb1-105">Busca la primera aparición de una subcadena terminada en null en una cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="97fb1-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="97fb1-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="97fb1-106">Header file:</span></span>  <br/> |<span data-ttu-id="97fb1-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="97fb1-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="97fb1-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="97fb1-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="97fb1-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="97fb1-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="97fb1-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="97fb1-110">Called by:</span></span>  <br/> |<span data-ttu-id="97fb1-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="97fb1-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="97fb1-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="97fb1-112">Parameters</span></span>

 <span data-ttu-id="97fb1-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="97fb1-113">_lpsz_</span></span>
  
> <span data-ttu-id="97fb1-114">[entrada] Puntero a la cadena terminada en null que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="97fb1-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="97fb1-115">El parámetro _lpsz_ no debe superar los caracteres, de 65536.</span><span class="sxs-lookup"><span data-stu-id="97fb1-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="97fb1-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="97fb1-116">_lpszKey_</span></span>
  
> <span data-ttu-id="97fb1-117">[entrada] Puntero a la subcadena terminada en null que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="97fb1-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="97fb1-118">El parámetro _lpszKey_ no debe superar los caracteres, de 65536.</span><span class="sxs-lookup"><span data-stu-id="97fb1-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="97fb1-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="97fb1-119">Return value</span></span>

 <span data-ttu-id="97fb1-120">**SzFindSz** devuelve un puntero al primer carácter de la primera aparición de la subcadena en la cadena.</span><span class="sxs-lookup"><span data-stu-id="97fb1-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="97fb1-121">Si la subcadena no se producen en cualquier lugar en la cadena, si _lpszKey_ es mayor que _lpsz_o si ninguno de estos parámetros es NULL, se devuelve un valor null.</span><span class="sxs-lookup"><span data-stu-id="97fb1-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="97fb1-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="97fb1-122">Remarks</span></span>

<span data-ttu-id="97fb1-123">La función **SzFindSz** busca una coincidencia exacta solamente; es sensible a mayúsculas y minúsculas y diferencias diacríticas.</span><span class="sxs-lookup"><span data-stu-id="97fb1-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="97fb1-124">Se admiten las búsquedas en formatos de Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="97fb1-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="97fb1-125">Es el límite de longitud en ambos parámetros en caracteres, no necesariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="97fb1-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

