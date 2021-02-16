---
title: IMAPIFormInfoSaveForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormInfo.SaveForm
api_type:
- COM
ms.assetid: 18a10f14-0795-4d4d-b590-f4cef4f2902a
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 391ea3ef4f44db2a9d007241232f58db27647ba2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428749"
---
# <a name="imapiforminfosaveform"></a><span data-ttu-id="361fe-103">IMAPIFormInfo::SaveForm</span><span class="sxs-lookup"><span data-stu-id="361fe-103">IMAPIFormInfo::SaveForm</span></span>

  
  
<span data-ttu-id="361fe-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="361fe-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="361fe-105">Guarda una descripción de un formulario determinado en un archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="361fe-105">Saves a description of a particular form in a configuration file.</span></span>
  
```cpp
HRESULT SaveForm(
  LPCSTR szFileName
);
```

## <a name="parameters"></a><span data-ttu-id="361fe-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="361fe-106">Parameters</span></span>

 <span data-ttu-id="361fe-107">_szFileName_</span><span class="sxs-lookup"><span data-stu-id="361fe-107">_szFileName_</span></span>
  
> <span data-ttu-id="361fe-108">[entrada] Cadena que nombra el archivo de mensaje de descripción del formulario donde se guarda su descripción.</span><span class="sxs-lookup"><span data-stu-id="361fe-108">[in] A string that names the form's description message file where its description is saved.</span></span> <span data-ttu-id="361fe-109">Este nombre de archivo debe tener la extensión .fdm.</span><span class="sxs-lookup"><span data-stu-id="361fe-109">This file name must have the .fdm extension.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="361fe-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="361fe-110">Return value</span></span>

<span data-ttu-id="361fe-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="361fe-111">S_OK</span></span> 
  
> <span data-ttu-id="361fe-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="361fe-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="361fe-113">MAPI_E_EXTENDED_ERROR</span><span class="sxs-lookup"><span data-stu-id="361fe-113">MAPI_E_EXTENDED_ERROR</span></span> 
  
> <span data-ttu-id="361fe-114">No se pudo escribir el archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="361fe-114">The configuration file could not be written.</span></span> <span data-ttu-id="361fe-115">Para obtener la [estructura MAPIERROR](mapierror.md) asociada al error, llame al método [IMAPIProp::GetLastError.](imapiprop-getlasterror.md)</span><span class="sxs-lookup"><span data-stu-id="361fe-115">To get the [MAPIERROR](mapierror.md) structure that is associated with the error, call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method.</span></span> 
    
<span data-ttu-id="361fe-116">MAPI_E_NO_SUPPORT</span><span class="sxs-lookup"><span data-stu-id="361fe-116">MAPI_E_NO_SUPPORT</span></span> 
  
> <span data-ttu-id="361fe-117">**Probablemente se llamó** a SaveForm para guardar un formulario en el contenedor de formularios local.</span><span class="sxs-lookup"><span data-stu-id="361fe-117">**SaveForm** was probably called to save a form in the local form container.</span></span> <span data-ttu-id="361fe-118">**SaveForm** no se admite en el contenedor de formularios local.</span><span class="sxs-lookup"><span data-stu-id="361fe-118">**SaveForm** is not supported on the local form container.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="361fe-119">Comentarios</span><span class="sxs-lookup"><span data-stu-id="361fe-119">Remarks</span></span>

<span data-ttu-id="361fe-120">Las aplicaciones cliente llaman al método **IMAPIFormInfo::SaveForm** para guardar una descripción del formulario actual en el archivo que tiene el nombre de archivo especificado.</span><span class="sxs-lookup"><span data-stu-id="361fe-120">Client applications call the **IMAPIFormInfo::SaveForm** method to save a description of the current form in the file that has the given file name.</span></span> <span data-ttu-id="361fe-121">**SaveForm** crea un archivo de configuración.</span><span class="sxs-lookup"><span data-stu-id="361fe-121">**SaveForm** creates a configuration file.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="361fe-122">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="361fe-122">Notes to callers</span></span>

<span data-ttu-id="361fe-123">Puede volver a instalar los formularios seleccionándolos en una lista de mensajes descriptores de formulario en un cuadro de diálogo que muestran los proveedores de bibliotecas de formularios.</span><span class="sxs-lookup"><span data-stu-id="361fe-123">You can reinstall forms by selecting them from a list of form descriptor messages in a dialog box that form library providers display.</span></span> <span data-ttu-id="361fe-124">La extensión recomendada para los mensajes del descriptor de formulario es .fdm.</span><span class="sxs-lookup"><span data-stu-id="361fe-124">The recommended extension for form descriptor messages is .fdm.</span></span>
  
<span data-ttu-id="361fe-125">Llame al [método IMAPIProp::GetLastError](imapiprop-getlasterror.md) si **SaveForm** devuelve MAPI_E_EXTENDED_ERROR y compruebe la estructura **MAPIERROR** devuelta para determinar la condición que provocó el error.</span><span class="sxs-lookup"><span data-stu-id="361fe-125">Call the [IMAPIProp::GetLastError](imapiprop-getlasterror.md) method if **SaveForm** returns MAPI_E_EXTENDED_ERROR, and check the returned **MAPIERROR** structure to determine the condition that caused the error.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="361fe-126">Consulte también</span><span class="sxs-lookup"><span data-stu-id="361fe-126">See also</span></span>



[<span data-ttu-id="361fe-127">IMAPIProp::GetLastError</span><span class="sxs-lookup"><span data-stu-id="361fe-127">IMAPIProp::GetLastError</span></span>](imapiprop-getlasterror.md)
  
[<span data-ttu-id="361fe-128">MAPIERROR</span><span class="sxs-lookup"><span data-stu-id="361fe-128">MAPIERROR</span></span>](mapierror.md)
  
[<span data-ttu-id="361fe-129">IMAPIFormInfo : IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="361fe-129">IMAPIFormInfo : IMAPIProp</span></span>](imapiforminfoimapiprop.md)

