---
title: MNLS_WideCharToMultiByte
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f64cde12-7ed1-444f-8ca4-51cb3ea514cf
description: 'Última modificación: 21 de febrero de 2012'
ms.openlocfilehash: f5cb63ca3d421073b00a448f762ecf0137494f2a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818417"
---
# <a name="mnlswidechartomultibyte"></a><span data-ttu-id="503da-103">MNLS_WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="503da-103">MNLS_WideCharToMultiByte</span></span>

  
  
<span data-ttu-id="503da-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="503da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="503da-105">Esta función es similar a **WideCharToMultiByte**, que se asigna una cadena de UTF-16 (carácter ancho) a una nueva cadena de caracteres.</span><span class="sxs-lookup"><span data-stu-id="503da-105">This function is similar to **WideCharToMultiByte**, which maps a UTF-16 (wide character) string to a new character string.</span></span> <span data-ttu-id="503da-106">La nueva cadena de caracteres no está necesariamente desde un carácter de varios bytes establecida.</span><span class="sxs-lookup"><span data-stu-id="503da-106">The new character string is not necessarily from a multibyte character set.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="503da-107">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="503da-107">Parameters</span></span>

 <span data-ttu-id="503da-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="503da-108">_uCodePage_</span></span>
  
> <span data-ttu-id="503da-109">[entrada] Página de códigos a utilizar para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="503da-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="503da-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="503da-110">_dwFlags_</span></span>
  
> <span data-ttu-id="503da-111">[entrada] Marcas que indica el tipo de conversión.</span><span class="sxs-lookup"><span data-stu-id="503da-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="503da-112">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="503da-112">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="503da-113">[entrada] Puntero a la cadena Unicode para convertir.</span><span class="sxs-lookup"><span data-stu-id="503da-113">[in] Pointer to the Unicode string to convert.</span></span>
    
 <span data-ttu-id="503da-114">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="503da-114">_cchWideChar_</span></span>
  
> <span data-ttu-id="503da-115">[entrada] Marcas que indica el tipo de conversión.</span><span class="sxs-lookup"><span data-stu-id="503da-115">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="503da-116">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="503da-116">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="503da-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="503da-117">[out] Optional.</span></span> <span data-ttu-id="503da-118">Puntero a un búfer que recibe la cadena convertida.</span><span class="sxs-lookup"><span data-stu-id="503da-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="503da-119">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="503da-119">_cchMultiByte_</span></span>
  
> <span data-ttu-id="503da-120">[entrada] Tamaño, en bytes, del búfer indicado por _lpMultiByteStr_.</span><span class="sxs-lookup"><span data-stu-id="503da-120">[in] Size, in bytes, of the buffer indicated by  _lpMultiByteStr_.</span></span>
    
 <span data-ttu-id="503da-121">_lpDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="503da-121">_lpDefaultChar_</span></span>
  
> <span data-ttu-id="503da-122">[in] Opcional.</span><span class="sxs-lookup"><span data-stu-id="503da-122">[in] Optional.</span></span> <span data-ttu-id="503da-123">Puntero al carácter que se va a usar si no se puede representar un carácter en la página de código especificado.</span><span class="sxs-lookup"><span data-stu-id="503da-123">Pointer to the character to use if a character cannot be represented in the specified code page.</span></span>
    
 <span data-ttu-id="503da-124">_lpfUsedDefaultChar_</span><span class="sxs-lookup"><span data-stu-id="503da-124">_lpfUsedDefaultChar_</span></span>
  
> <span data-ttu-id="503da-125">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="503da-125">[out] Optional.</span></span> <span data-ttu-id="503da-126">Puntero a una marca que indica si la función ha usado un carácter predeterminado en la conversión.</span><span class="sxs-lookup"><span data-stu-id="503da-126">Pointer to a flag that indicates if the function has used a default character in the conversion.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="503da-127">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="503da-127">Return value</span></span>

<span data-ttu-id="503da-128">Devuelve el número de bytes escritos en el búfer al que señala por _lpMultiByteStr_ si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="503da-128">Returns the number of bytes written to the buffer pointed to by  _lpMultiByteStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="503da-129">Notas</span><span class="sxs-lookup"><span data-stu-id="503da-129">Remarks</span></span>

<span data-ttu-id="503da-130">Esta función ajusta la función **WideCharToMultiByte** .</span><span class="sxs-lookup"><span data-stu-id="503da-130">This function wraps the **WideCharToMultiByte** function.</span></span> <span data-ttu-id="503da-131">Para obtener más información, vea [WideCharToMultiByte](http://msdn.microsoft.com/es-es/library/dd374130%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="503da-131">For more information, see [WideCharToMultiByte](http://msdn.microsoft.com/es-es/library/dd374130%28VS.85%29.aspx).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="503da-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="503da-132">See also</span></span>



[<span data-ttu-id="503da-133">WideCharToMultiByte</span><span class="sxs-lookup"><span data-stu-id="503da-133">WideCharToMultiByte</span></span>](http://msdn.microsoft.com/es-es/library/dd374130%28VS.85%29.aspx)

