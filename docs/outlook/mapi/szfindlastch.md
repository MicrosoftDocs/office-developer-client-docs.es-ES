---
title: SzFindLastCh
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.SzFindLastCh
api_type:
- COM
ms.assetid: 7c3e5a71-7b78-4328-b8ee-265cc4da4be5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: eeeff110e5de592d491865079adfa187e5dfa194
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570880"
---
# <a name="szfindlastch"></a><span data-ttu-id="a1b19-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="a1b19-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="a1b19-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a1b19-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a1b19-105">Busca la última aparición de un carácter en una cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="a1b19-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a1b19-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a1b19-106">Header file:</span></span>  <br/> |<span data-ttu-id="a1b19-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a1b19-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a1b19-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="a1b19-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a1b19-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a1b19-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a1b19-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a1b19-110">Called by:</span></span>  <br/> |<span data-ttu-id="a1b19-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a1b19-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="a1b19-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a1b19-112">Parameters</span></span>

 <span data-ttu-id="a1b19-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a1b19-113">_lpsz_</span></span>
  
> <span data-ttu-id="a1b19-114">[entrada] Puntero a la cadena terminada en null que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="a1b19-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="a1b19-115">_canales_</span><span class="sxs-lookup"><span data-stu-id="a1b19-115">_ch_</span></span>
  
> <span data-ttu-id="a1b19-116">[entrada] El carácter que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="a1b19-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a1b19-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a1b19-117">Return value</span></span>

 <span data-ttu-id="a1b19-118">**SzFindLastCh** devuelve un puntero a la última aparición del carácter en la cadena.</span><span class="sxs-lookup"><span data-stu-id="a1b19-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="a1b19-119">Si el carácter no se produce en cualquier lugar en la cadena, o si el parámetro _lpsz_ es NULL, se devuelve un valor null.</span><span class="sxs-lookup"><span data-stu-id="a1b19-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a1b19-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a1b19-120">Remarks</span></span>

<span data-ttu-id="a1b19-121">La función **SzFindLastCh** busca una coincidencia exacta solamente; es sensible a mayúsculas y minúsculas y diferencias diacríticas.</span><span class="sxs-lookup"><span data-stu-id="a1b19-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="a1b19-122">Se admiten las búsquedas en los formatos de Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="a1b19-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

