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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 8426f782eb5fbf8a125833c51b25ccd605acbd64
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573526"
---
# <a name="szfindch"></a><span data-ttu-id="1832f-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="1832f-103">SzFindCh</span></span>
 
<span data-ttu-id="1832f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1832f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1832f-105">Busca la primera aparición de un carácter en una cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="1832f-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="1832f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="1832f-106">Header file:</span></span>  <br/> |<span data-ttu-id="1832f-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="1832f-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="1832f-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="1832f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="1832f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="1832f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="1832f-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="1832f-110">Called by:</span></span>  <br/> |<span data-ttu-id="1832f-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="1832f-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="1832f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="1832f-112">Parameters</span></span>

<span data-ttu-id="1832f-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="1832f-113">_lpsz_</span></span>
  
> <span data-ttu-id="1832f-114">[entrada] Puntero a la cadena terminada en null que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="1832f-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="1832f-115">_canales_</span><span class="sxs-lookup"><span data-stu-id="1832f-115">_ch_</span></span>
  
> <span data-ttu-id="1832f-116">[entrada] El carácter que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="1832f-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1832f-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1832f-117">Return value</span></span>

<span data-ttu-id="1832f-118">**SzFindCh** devuelve un puntero a la primera aparición del carácter en la cadena.</span><span class="sxs-lookup"><span data-stu-id="1832f-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="1832f-119">Si el carácter no se produce en cualquier lugar en la cadena, o si el parámetro _lpsz_ es NULL, se devuelve un valor null.</span><span class="sxs-lookup"><span data-stu-id="1832f-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="1832f-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1832f-120">Remarks</span></span>

<span data-ttu-id="1832f-121">La función **SzFindCh** busca una coincidencia exacta solamente; es sensible a mayúsculas y minúsculas y diferencias diacríticas.</span><span class="sxs-lookup"><span data-stu-id="1832f-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="1832f-122">Se admiten las búsquedas en los formatos de Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="1832f-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

