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
ms.openlocfilehash: ab082c8ac70bf851097080fb41033f76bccc3044
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818407"
---
# <a name="mnlsmultibytetowidechar"></a><span data-ttu-id="d52bf-103">MNLS_MultiByteToWideChar</span><span class="sxs-lookup"><span data-stu-id="d52bf-103">MNLS_MultiByteToWideChar</span></span>

  
  
<span data-ttu-id="d52bf-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d52bf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d52bf-105">Es similar a **MultiByteToWideChar**, que se asigna una cadena de caracteres en una cadena de UTF-16 (carácter ancho).</span><span class="sxs-lookup"><span data-stu-id="d52bf-105">Similar to **MultiByteToWideChar**, which maps a character string to a UTF-16 (wide character) string.</span></span> <span data-ttu-id="d52bf-106">La cadena de caracteres no está necesariamente desde un carácter de varios bytes establecida.</span><span class="sxs-lookup"><span data-stu-id="d52bf-106">The character string is not necessarily from a multibyte character set.</span></span>
  
```cpp
int MNLS_MultiByteToWideChar(
  UINT uCodePage,
  DWORD dwFlags,
  LPCSTR lpMultiByteStr,
  int cchMultiByte,
  LPWSTR lpWideCharStr,
  int cchWideChar);
```

## <a name="parameters"></a><span data-ttu-id="d52bf-107">Parámetros</span><span class="sxs-lookup"><span data-stu-id="d52bf-107">Parameters</span></span>

 <span data-ttu-id="d52bf-108">_uCodePage_</span><span class="sxs-lookup"><span data-stu-id="d52bf-108">_uCodePage_</span></span>
  
> <span data-ttu-id="d52bf-109">[entrada] Página de códigos a utilizar para realizar la conversión.</span><span class="sxs-lookup"><span data-stu-id="d52bf-109">[in] Code page to use in performing the conversion.</span></span>
    
 <span data-ttu-id="d52bf-110">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="d52bf-110">_dwFlags_</span></span>
  
> <span data-ttu-id="d52bf-111">[entrada] Marcas que indica el tipo de conversión.</span><span class="sxs-lookup"><span data-stu-id="d52bf-111">[in] Flags indicating the conversion type.</span></span>
    
 <span data-ttu-id="d52bf-112">_lpMultiByteStr_</span><span class="sxs-lookup"><span data-stu-id="d52bf-112">_lpMultiByteStr_</span></span>
  
> <span data-ttu-id="d52bf-113">[entrada] Puntero a la cadena de caracteres para convertir.</span><span class="sxs-lookup"><span data-stu-id="d52bf-113">[in] Pointer to the character string to convert.</span></span>
    
 <span data-ttu-id="d52bf-114">_cchMultiByte_</span><span class="sxs-lookup"><span data-stu-id="d52bf-114">_cchMultiByte_</span></span>
  
> <span data-ttu-id="d52bf-115">[entrada] Tamaño, en bytes, de la cadena indicada por el parámetro _lpMultiByteStr_ .</span><span class="sxs-lookup"><span data-stu-id="d52bf-115">[in] Size, in bytes, of the string indicated by the  _lpMultiByteStr_ parameter.</span></span> 
    
 <span data-ttu-id="d52bf-116">_lpWideCharStr_</span><span class="sxs-lookup"><span data-stu-id="d52bf-116">_lpWideCharStr_</span></span>
  
> <span data-ttu-id="d52bf-117">[out] Opcional.</span><span class="sxs-lookup"><span data-stu-id="d52bf-117">[out] Optional.</span></span> <span data-ttu-id="d52bf-118">Puntero a un búfer que recibe la cadena convertida.</span><span class="sxs-lookup"><span data-stu-id="d52bf-118">Pointer to a buffer that receives the converted string.</span></span>
    
 <span data-ttu-id="d52bf-119">_cchWideChar_</span><span class="sxs-lookup"><span data-stu-id="d52bf-119">_cchWideChar_</span></span>
  
> <span data-ttu-id="d52bf-120">[entrada] Tamaño, en caracteres, del búfer indicado por _lpWideCharStr_.</span><span class="sxs-lookup"><span data-stu-id="d52bf-120">[in] Size, in characters, of the buffer indicated by  _lpWideCharStr_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d52bf-121">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d52bf-121">Return value</span></span>

<span data-ttu-id="d52bf-122">Devuelve el número de caracteres escritos en el búfer indicado por _lpWideCharStr_ si se realiza correctamente.</span><span class="sxs-lookup"><span data-stu-id="d52bf-122">Returns the number of characters written to the buffer indicated by  _lpWideCharStr_ if successful.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="d52bf-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d52bf-123">Remarks</span></span>

<span data-ttu-id="d52bf-124">Esta función ajusta la función **MultiByteToWideChar** .</span><span class="sxs-lookup"><span data-stu-id="d52bf-124">This function wraps the **MultiByteToWideChar** function.</span></span> <span data-ttu-id="d52bf-125">Para obtener más información, vea [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="d52bf-125">For more information, see [MultiByteToWideChar](http://msdn.microsoft.com/en-us/library/dd319072%28VS.85%29.aspx).</span></span>
  

