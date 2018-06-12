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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: c221f98d6551ea63971dd378d522c1f2bebb312b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820830"
---
# <a name="szfindlastch"></a><span data-ttu-id="ae7b3-103">SzFindLastCh</span><span class="sxs-lookup"><span data-stu-id="ae7b3-103">SzFindLastCh</span></span>

  
  
<span data-ttu-id="ae7b3-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ae7b3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ae7b3-105">Busca la última aparición de un carácter en una cadena terminada en null.</span><span class="sxs-lookup"><span data-stu-id="ae7b3-105">Searches for the last occurrence of a character in a null-terminated string.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="ae7b3-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="ae7b3-106">Header file:</span></span>  <br/> |<span data-ttu-id="ae7b3-107">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ae7b3-107">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="ae7b3-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="ae7b3-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="ae7b3-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="ae7b3-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="ae7b3-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="ae7b3-110">Called by:</span></span>  <br/> |<span data-ttu-id="ae7b3-111">Las aplicaciones cliente y los proveedores de servicios</span><span class="sxs-lookup"><span data-stu-id="ae7b3-111">Client applications and service providers</span></span>  <br/> |
   
```cpp
LPSTR SzFindLastCh(
  LPCSTR lpsz,
  USHORT ch
);
```

## <a name="parameters"></a><span data-ttu-id="ae7b3-112">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="ae7b3-112">Parameters</span></span>

 <span data-ttu-id="ae7b3-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="ae7b3-113">_lpsz_</span></span>
  
> <span data-ttu-id="ae7b3-114">[entrada] Puntero a la cadena terminada en null que se desea buscar.</span><span class="sxs-lookup"><span data-stu-id="ae7b3-114">[in] Pointer to the null-terminated string to be searched.</span></span> 
    
 <span data-ttu-id="ae7b3-115">_canales_</span><span class="sxs-lookup"><span data-stu-id="ae7b3-115">_ch_</span></span>
  
> <span data-ttu-id="ae7b3-116">[entrada] El carácter que se va a buscar.</span><span class="sxs-lookup"><span data-stu-id="ae7b3-116">[in] The character to be searched for.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ae7b3-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ae7b3-117">Return value</span></span>

 <span data-ttu-id="ae7b3-118">**SzFindLastCh** devuelve un puntero a la última aparición del carácter en la cadena.</span><span class="sxs-lookup"><span data-stu-id="ae7b3-118">**SzFindLastCh** returns a pointer to the last occurrence of the character in the string.</span></span> <span data-ttu-id="ae7b3-119">Si el carácter no se produce en cualquier lugar en la cadena, o si el parámetro _lpsz_ es NULL, se devuelve un valor null.</span><span class="sxs-lookup"><span data-stu-id="ae7b3-119">If the character does not occur anywhere in the string, or if the  _lpsz_ parameter is NULL, a value of NULL is returned.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="ae7b3-120">Notas</span><span class="sxs-lookup"><span data-stu-id="ae7b3-120">Remarks</span></span>

<span data-ttu-id="ae7b3-121">La función **SzFindLastCh** busca una coincidencia exacta solamente; es sensible a mayúsculas y minúsculas y diferencias diacríticas.</span><span class="sxs-lookup"><span data-stu-id="ae7b3-121">The **SzFindLastCh** function searches for an exact match only; it is sensitive to case and diacritical differences.</span></span> <span data-ttu-id="ae7b3-122">Se admiten las búsquedas en los formatos de Unicode y DBCS.</span><span class="sxs-lookup"><span data-stu-id="ae7b3-122">Searches in the Unicode and DBCS formats are supported.</span></span> 
  

