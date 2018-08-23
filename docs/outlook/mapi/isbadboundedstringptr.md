---
title: IsBadBoundedStringPtr
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 888c60e3-7376-4d66-8ee2-ce81abafb185
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 39b4474bcc6bd71993fb5dc42bb2bfc1bf9f5f48
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573407"
---
# <a name="isbadboundedstringptr"></a><span data-ttu-id="d698f-103">IsBadBoundedStringPtr</span><span class="sxs-lookup"><span data-stu-id="d698f-103">IsBadBoundedStringPtr</span></span>

  
  
<span data-ttu-id="d698f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d698f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d698f-105">Comprueba que el proceso de llamada tiene acceso de lectura para el intervalo de memoria especificado.</span><span class="sxs-lookup"><span data-stu-id="d698f-105">Verifies that the calling process has read access to the specified range of memory.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="d698f-106">Archivo de encabezado:</span><span class="sxs-lookup"><span data-stu-id="d698f-106">Header file:</span></span>  <br/> |<span data-ttu-id="d698f-107">mapiwin.h</span><span class="sxs-lookup"><span data-stu-id="d698f-107">mapiwin.h</span></span>  <br/> |
|<span data-ttu-id="d698f-108">Se implementa mediante:</span><span class="sxs-lookup"><span data-stu-id="d698f-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="d698f-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="d698f-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="d698f-110">Llamado por:</span><span class="sxs-lookup"><span data-stu-id="d698f-110">Called by:</span></span>  <br/> |<span data-ttu-id="d698f-111">Las aplicaciones de cliente y los proveedores de servicios.</span><span class="sxs-lookup"><span data-stu-id="d698f-111">Client applications and service providers.</span></span>  <br/> |
   
```cpp
BOOL IsBadBoundedStringPtr(
  const void FAR* lpsz,
  UINT cchMax
);
```

## <a name="parameters"></a><span data-ttu-id="d698f-112">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d698f-112">Parameters</span></span>

 <span data-ttu-id="d698f-113">_lpsz_</span><span class="sxs-lookup"><span data-stu-id="d698f-113">_lpsz_</span></span>
  
> <span data-ttu-id="d698f-114">[entrada] Puntero a una cadena ASCII terminada en null.</span><span class="sxs-lookup"><span data-stu-id="d698f-114">[in] Pointer to a null-terminated ASCII string.</span></span>
    
 <span data-ttu-id="d698f-115">_cchMax_</span><span class="sxs-lookup"><span data-stu-id="d698f-115">_cchMax_</span></span>
  
> <span data-ttu-id="d698f-116">[entrada] El tamaño máximo de la cadena en caracteres.</span><span class="sxs-lookup"><span data-stu-id="d698f-116">[in] The maximum size of the string, in CHARs.</span></span> <span data-ttu-id="d698f-117">La función comprueba para acceso de lectura en todos los caracteres hasta el carácter null de terminación de la cadena o el número máximo de caracteres especificado por este parámetro, lo que sea menor.</span><span class="sxs-lookup"><span data-stu-id="d698f-117">The function checks for read access in all characters up to the terminating null character of the string, or up to the number of characters specified by this parameter, whichever is smaller.</span></span> <span data-ttu-id="d698f-118">Si este parámetro es cero, el valor devuelto es cero.</span><span class="sxs-lookup"><span data-stu-id="d698f-118">If this parameter is zero, the return value is zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d698f-119">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d698f-119">Return value</span></span>

<span data-ttu-id="d698f-120">El valor devuelto es cero cuando el proceso de llamada tiene acceso de lectura a todos los caracteres hasta el carácter null de terminación de la cadena o acceso de lectura hasta el número de caracteres especificado por _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="d698f-120">The return value is zero when the calling process has read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
<span data-ttu-id="d698f-121">El valor devuelto es distinto de cero cuando el proceso de llamada no tiene acceso de lectura a todos los caracteres hasta el carácter null de terminación de la cadena o acceso de lectura hasta el número de caracteres especificado por _cchMax_.</span><span class="sxs-lookup"><span data-stu-id="d698f-121">The return value is non-zero when the calling process does not have read access to all characters up to the terminating null character of the string, or read access up to the number of characters specified by  _cchMax_.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d698f-122">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d698f-122">Remarks</span></span>

<span data-ttu-id="d698f-123">La función **IsBadBoundedStringPtr** equivale a usar **IsBadStringPtr**.</span><span class="sxs-lookup"><span data-stu-id="d698f-123">The **IsBadBoundedStringPtr** function is equivalent to using **IsBadStringPtr**.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="d698f-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="d698f-124">See also</span></span>



[<span data-ttu-id="d698f-125">IsBadStringPtr</span><span class="sxs-lookup"><span data-stu-id="d698f-125">IsBadStringPtr</span></span>](http://msdn.microsoft.com/en-us/library/windows/desktop/aa366714%28v=vs.85%29.aspx)

