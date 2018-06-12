---
title: SzFindCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindCh
api_type:
- COM
ms.assetid: 3406d060-bfea-4cea-8253-2a9aeb9e8147
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: b517eaffa56001d8c414888ee6cbc8ec4f49cf66
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820828"
---
# <a name="szfindch"></a><span data-ttu-id="35a6c-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="35a6c-103">SzFindCh</span></span>
 
<span data-ttu-id="35a6c-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="35a6c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="35a6c-105">Busca la primera aparición de un carácter en una cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="35a6c-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="35a6c-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="35a6c-106">Header file:</span></span>  <br/> |<span data-ttu-id="35a6c-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="35a6c-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="35a6c-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="35a6c-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="35a6c-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="35a6c-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="35a6c-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="35a6c-110">Called by:</span></span>  <br/> |<span data-ttu-id="35a6c-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="35a6c-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="35a6c-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="35a6c-112">Parameters</span></span>

<span data-ttu-id="35a6c-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="35a6c-113">_lpsz_</span></span>
  
> <span data-ttu-id="35a6c-114">[entrada] Puntero a la cadena terminada en null que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="35a6c-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="35a6c-115">_canales_</span><span class="sxs-lookup"><span data-stu-id="35a6c-115">_ch_</span></span>
  
> <span data-ttu-id="35a6c-116">[entrada] El carácter que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="35a6c-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="35a6c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="35a6c-117">Return value</span></span>

<span data-ttu-id="35a6c-118">**SzFindCh** devuelve un puntero a la primera aparición del carácter en la cadena.</span><span class="sxs-lookup"><span data-stu-id="35a6c-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="35a6c-119">Si el carácter no se produce en cualquier lugar en la cadena, o si el parámetro _lpsz_ es NULL, se devuelve un valor null.</span><span class="sxs-lookup"><span data-stu-id="35a6c-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="35a6c-120">Notas</span><span class="sxs-lookup"><span data-stu-id="35a6c-120">Remarks</span></span>

<span data-ttu-id="35a6c-121">La función **SzFindCh** busca una coincidencia exacta solamente; es sensible a mayúsculas y minúsculas y diferencias diacríticas.</span><span class="sxs-lookup"><span data-stu-id="35a6c-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="35a6c-122">Se admiten las búsquedas en los formatos de Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="35a6c-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

