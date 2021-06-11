---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Last modified: February 21, 2012'
ms.openlocfilehash: ad41f9b6060e5cfbabecfd9bb29a47815929d6b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338734"
---
# <a name="mnls_widechartomultibyte"></a><span data-ttu-id="af104-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="af104-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="af104-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="af104-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="af104-105">Esta función es similar a **WideCharToMultiByte**, que asigna una cadena UTF-16 (carácter ancho) a una nueva cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="af104-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="af104-106">La nueva cadena de caracteres no es necesariamente de un conjunto de caracteres multibyte.</span><span class="sxs-lookup"><span data-stu-id="af104-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_WideCharToMultiByte(
  UINT uCodePage,
  DWORD dwFlags,
  LPCWSTR lpWideCharStr,
  int cchWideChar,
  LPSTR lpMultiByteStr,
  int cchMultiByte,
  LPCSTR lpDefaultChar,
  BOOL FAR *lpfUsedDefaultChar);
```

## <a name="parameters"></a><span data-ttu-id="af104-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="af104-107">Parameters</span></span>

 <span data-ttu-id="af104-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="af104-108">_uCodePage_</span></span>
  
> <span data-ttu-id="af104-109">[in] Página de código que se usará para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="af104-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="af104-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="af104-110">_dwFlags_</span></span>
  
> <span data-ttu-id="af104-111">[in] Marcas que indican el tipo de conversión.</span><span class="sxs-lookup"><span data-stu-id="af104-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="af104-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="af104-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="af104-113">[in] Puntero a la cadena Unicode que se debe convertir.</span><span class="sxs-lookup"><span data-stu-id="af104-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="af104-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="af104-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="af104-115">[in] Marcas que indican el tipo de conversión.</span><span class="sxs-lookup"><span data-stu-id="af104-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="af104-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="af104-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="af104-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="af104-117">[out] Optional.</span></span> <span data-ttu-id="af104-118">Puntero a un búfer que recibe la cadena convertida.</span><span class="sxs-lookup"><span data-stu-id="af104-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="af104-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="af104-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="af104-120">[in] Tamaño, en bytes, del búfer indicado por  _lpMultiByteStr_.</span><span class="sxs-lookup"><span data-stu-id="af104-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="af104-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="af104-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="af104-122">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="af104-122">[in] Optional.</span></span> <span data-ttu-id="af104-123">Puntero al carácter que se va a usar si no se puede representar un carácter en la página de códigos especificada.</span><span class="sxs-lookup"><span data-stu-id="af104-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="af104-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="af104-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="af104-125">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="af104-125">[out] Optional.</span></span> <span data-ttu-id="af104-126">Puntero a una marca que indica si la función ha usado un carácter predeterminado en la conversión.</span><span class="sxs-lookup"><span data-stu-id="af104-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="af104-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="af104-127">Return value</span></span>

<span data-ttu-id="af104-128">Devuelve el número de bytes escritos en el búfer al que  _apunta lpMultiByteStr_ si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="af104-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="af104-129">Comentarios</span><span class="sxs-lookup"><span data-stu-id="af104-129">Remarks</span></span>

<span data-ttu-id="af104-130">Esta función ajusta la **función WideCharToMultiByte.**</span><span class="sxs-lookup"><span data-stu-id="af104-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="af104-131">Para obtener más información, [vea WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="af104-131">For more information, see [WideCharToMultiByte](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="af104-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="af104-132">See also</span></span>



[<span data-ttu-id="af104-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="af104-133">WideCharToMultiByte</span></span>](https://msdn.microsoft.com/library/dd374130%28VS.85%29.aspx)

