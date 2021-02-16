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
ms.openlocfilehash: 9fc21a27cb6c9041bdd8976ce5f030f0ab9eb57f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435225"
---
# <a name="szfindsz"></a><span data-ttu-id="db6af-103">SzFindSz</span><span class="sxs-lookup"><span data-stu-id="db6af-103">SzFindSz</span></span>

  
  
<span data-ttu-id="db6af-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="db6af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="db6af-105">Busca la primera aparición de una subcadena terminada en null en una cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="db6af-105">Locates the first occurrence of a null-terminated substring in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="db6af-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="db6af-106">Header file:</span></span>  <br/> |<span data-ttu-id="db6af-107">Mapiutil.h</span><span class="sxs-lookup"><span data-stu-id="db6af-107">Mapiutil.h</span></span>  <br/> |
|<span data-ttu-id="db6af-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="db6af-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="db6af-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="db6af-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="db6af-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="db6af-110">Called by:</span></span>  <br/> |<span data-ttu-id="db6af-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="db6af-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  LPCSTR lpszKey
);
```

## <a name="parameters"></a><span data-ttu-id="db6af-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="db6af-112">Parameters</span></span>

 <span data-ttu-id="db6af-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="db6af-113">_lpsz_</span></span>
  
> <span data-ttu-id="db6af-114">[entrada] Puntero a la cadena terminada en null en la que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="db6af-114">[in] Pointer to the null-terminated string to be searched.</span></span> <span data-ttu-id="db6af-115">El  _parámetro lpsz_ no debe superar los 65536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="db6af-115">The  _lpsz_ parameter must not exceed 65536 characters.</span></span> 
    
 <span data-ttu-id="db6af-116">_lpszKey_</span><span class="sxs-lookup"><span data-stu-id="db6af-116">_lpszKey_</span></span>
  
> <span data-ttu-id="db6af-117">[entrada] Puntero a la subcadena terminada en null que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="db6af-117">[in] Pointer to the null-terminated substring to be searched for.</span></span> <span data-ttu-id="db6af-118">El  _parámetro lpszKey_ no debe superar los 65536 caracteres.</span><span class="sxs-lookup"><span data-stu-id="db6af-118">The  _lpszKey_ parameter must not exceed 65536 characters.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="db6af-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="db6af-119">Return value</span></span>

 <span data-ttu-id="db6af-120">**SzFindSz** devuelve un puntero al primer carácter de la primera aparición de la subcadena de la cadena.</span><span class="sxs-lookup"><span data-stu-id="db6af-120">**SzFindSz** returns a pointer to the first character of the first occurrence of the substring in the string.</span></span> <span data-ttu-id="db6af-121">Si la subcadena no se produce en ningún lugar de la cadena, si  _lpszKey_ es mayor que  _lpsz_ o si cualquiera de los parámetros es NULL, se devuelve un valor NULL.</span><span class="sxs-lookup"><span data-stu-id="db6af-121">If the substring does not occur anywhere in the string, if  _lpszKey_ is larger than  _lpsz_, or if either parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="db6af-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="db6af-122">Remarks</span></span>

<span data-ttu-id="db6af-123">La **función SzFindSz** solo busca una coincidencia exacta; es sensible a las diferencias entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="db6af-123">The **SzFindSz** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="db6af-124">Se admiten búsquedas en formatos Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="db6af-124">Searches in Unicode and DBCS formats are supported.</span></span> <span data-ttu-id="db6af-125">El límite de longitud de ambos parámetros está en caracteres, no necesariamente bytes.</span><span class="sxs-lookup"><span data-stu-id="db6af-125">The length limit on both parameters is in characters, not necessarily bytes.</span></span> 
  

