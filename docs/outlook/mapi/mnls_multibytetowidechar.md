---
title: MNLS_MultiByteToWideChar
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 065d78bf-4c9c-48dd-b1f1-b4e59f3f1243
description: 'Última modificación: 21 de febrero de 2012'
ms.openlocfilehash: 1f137aba40703fe84e5753ee6e370262f780f0a3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338244"
---
# <a name="mnls_multibytetowidechar"></a><span data-ttu-id="a579b-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="a579b-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="a579b-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a579b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a579b-105">Similar a **MultiByteToWideChar**, que asigna una cadena de caracteres a una cadena UTF-16 (carácter ancho).</span><span class="sxs-lookup"><span data-stu-id="a579b-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="a579b-106">La cadena de caracteres no es necesariamente de un juego de caracteres multibyte.</span><span class="sxs-lookup"><span data-stu-id="a579b-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="a579b-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="a579b-107">Parameters</span></span>

 <span data-ttu-id="a579b-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="a579b-108">_uCodePage_</span></span>
  
> <span data-ttu-id="a579b-109">[entrada] Página de códigos que se usará para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="a579b-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="a579b-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="a579b-110">_dwFlags_</span></span>
  
> <span data-ttu-id="a579b-111">[entrada] Marcas que indican el tipo de conversión.</span><span class="sxs-lookup"><span data-stu-id="a579b-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="a579b-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="a579b-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="a579b-113">[entrada] Puntero a la cadena de caracteres que se convertirá.</span><span class="sxs-lookup"><span data-stu-id="a579b-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="a579b-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="a579b-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="a579b-115">[entrada] Tamaño, en bytes, de la cadena indicada por el _parámetro lpMultiByteStr._</span><span class="sxs-lookup"><span data-stu-id="a579b-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="a579b-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="a579b-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="a579b-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="a579b-117">[out] Optional.</span></span> <span data-ttu-id="a579b-118">Puntero a un búfer que recibe la cadena convertida.</span><span class="sxs-lookup"><span data-stu-id="a579b-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="a579b-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="a579b-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="a579b-120">[entrada] Tamaño, en caracteres, del búfer indicado por  _lpWideCharStr_.</span><span class="sxs-lookup"><span data-stu-id="a579b-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a579b-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a579b-121">Return value</span></span>

<span data-ttu-id="a579b-122">Devuelve el número de caracteres escritos en el búfer indicado por  _lpWideCharStr_ si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="a579b-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="a579b-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a579b-123">Remarks</span></span>

<span data-ttu-id="a579b-124">Esta función encapsula la **función MultiByteToWideChar.**</span><span class="sxs-lookup"><span data-stu-id="a579b-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="a579b-125">Para obtener más información, [vea MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="a579b-125">For more information, see [MultiByteToWideChar](https://msdn.microsoft.com/library/dd319072%28VS.85%29.aspx).</span></span>
  

