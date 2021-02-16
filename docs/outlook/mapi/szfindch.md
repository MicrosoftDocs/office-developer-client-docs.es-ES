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
ms.openlocfilehash: 522c67b19656c00ea169def98a42ca2b3c1db840
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421945"
---
# <a name="szfindch"></a><span data-ttu-id="eee85-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="eee85-103">SzFindCh</span></span>
 
<span data-ttu-id="eee85-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eee85-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eee85-105">Busca la primera aparición de un carácter en una cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="eee85-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="eee85-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="eee85-106">Header file:</span></span>  <br/> |<span data-ttu-id="eee85-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="eee85-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="eee85-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="eee85-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="eee85-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="eee85-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="eee85-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="eee85-110">Called by:</span></span>  <br/> |<span data-ttu-id="eee85-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="eee85-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="eee85-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eee85-112">Parameters</span></span>

<span data-ttu-id="eee85-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="eee85-113">_lpsz_</span></span>
  
> <span data-ttu-id="eee85-114">[entrada] Puntero a la cadena terminada en null en la que se buscará.</span><span class="sxs-lookup"><span data-stu-id="eee85-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="eee85-115">_ch_</span><span class="sxs-lookup"><span data-stu-id="eee85-115">_ch_</span></span>
  
> <span data-ttu-id="eee85-116">[entrada] Carácter que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="eee85-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eee85-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eee85-117">Return value</span></span>

<span data-ttu-id="eee85-118">**SzFindCh** devuelve un puntero a la primera aparición del carácter de la cadena.</span><span class="sxs-lookup"><span data-stu-id="eee85-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="eee85-119">Si el carácter no se produce en ninguna parte de la cadena o si el parámetro  _lpsz_ es NULL, se devuelve un valor NULL.</span><span class="sxs-lookup"><span data-stu-id="eee85-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="eee85-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eee85-120">Remarks</span></span>

<span data-ttu-id="eee85-121">La **función SzFindCh** solo busca una coincidencia exacta; es sensible a las diferencias entre mayúsculas y minúsculas.</span><span class="sxs-lookup"><span data-stu-id="eee85-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="eee85-122">Se admiten búsquedas en los formatos Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="eee85-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

