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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345244"
---
# <a name="szfindch"></a><span data-ttu-id="a8996-103">SzFindCh</span><span class="sxs-lookup"><span data-stu-id="a8996-103">SzFindCh</span></span>
 
<span data-ttu-id="a8996-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a8996-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a8996-105">Busca la primera aparición de un carácter en una cadena terminada en NULL.</span><span class="sxs-lookup"><span data-stu-id="a8996-105">Searches for the first occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="a8996-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="a8996-106">Header file:</span></span>  <br/> |<span data-ttu-id="a8996-107">Mapidefs. h</span><span class="sxs-lookup"><span data-stu-id="a8996-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="a8996-108">Implementado por:</span><span class="sxs-lookup"><span data-stu-id="a8996-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="a8996-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="a8996-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="a8996-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="a8996-110">Called by:</span></span>  <br/> |<span data-ttu-id="a8996-111">Aplicaciones cliente y proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="a8996-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="a8996-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="a8996-112">Parameters</span></span>

<span data-ttu-id="a8996-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="a8996-113">_lpsz_</span></span>
  
> <span data-ttu-id="a8996-114">a Puntero a la cadena terminada en null en la que se va a realizar la búsqueda.</span><span class="sxs-lookup"><span data-stu-id="a8996-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
<span data-ttu-id="a8996-115">_CH_</span><span class="sxs-lookup"><span data-stu-id="a8996-115">_ch_</span></span>
  
> <span data-ttu-id="a8996-116">a El carácter que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="a8996-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a8996-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a8996-117">Return value</span></span>

<span data-ttu-id="a8996-118">**SzFindCh** devuelve un puntero a la primera aparición del carácter en la cadena.</span><span class="sxs-lookup"><span data-stu-id="a8996-118">**SzFindCh** returns a pointer to the first occurrence of the character in the string.</span></span> <span data-ttu-id="a8996-119">Si el carácter no aparece en ninguna parte de la cadena o si el parámetro _lpsz_ es null, se devuelve un valor null.</span><span class="sxs-lookup"><span data-stu-id="a8996-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a8996-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a8996-120">Remarks</span></span>

<span data-ttu-id="a8996-121">La función **SzFindCh** busca sólo una coincidencia exacta; es sensible a las diferencias de mayúsculas y minúsculas y diacríticos.</span><span class="sxs-lookup"><span data-stu-id="a8996-121">The **SzFindCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="a8996-122">Se admiten las búsquedas en los formatos Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="a8996-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

