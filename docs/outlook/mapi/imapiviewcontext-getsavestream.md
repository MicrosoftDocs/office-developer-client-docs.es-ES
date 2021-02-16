---
title: IMAPIViewContextGetSaveStream
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.GetSaveStream
api_type:
- COM
ms.assetid: 8316bfa1-3077-401f-aa1e-e9492aca12a8
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 68eb74f53d6cee4661c98604ec2ea37609e20ab5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408428"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="790c8-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="790c8-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="790c8-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="790c8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="790c8-105">Recupera una secuencia que se usará para guardar el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="790c8-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="790c8-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="790c8-106">Parameters</span></span>

 <span data-ttu-id="790c8-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="790c8-107">_pulFlags_</span></span>
  
> <span data-ttu-id="790c8-108">[salida] Puntero a una máscara de bits de marcas que controla cómo se debe guardar el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="790c8-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="790c8-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="790c8-109">The following flag can be set:</span></span>
    
<span data-ttu-id="790c8-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="790c8-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="790c8-111">El texto del mensaje se guarda en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="790c8-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="790c8-112">Si no MAPI_UNICODE marca, el texto se guarda en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="790c8-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="790c8-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="790c8-113">_pulFormat_</span></span>
  
> <span data-ttu-id="790c8-114">[salida] Puntero a una máscara de bits de marcas que controla el formato del texto guardado.</span><span class="sxs-lookup"><span data-stu-id="790c8-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="790c8-115">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="790c8-115">The following flags can be set:</span></span>
    
<span data-ttu-id="790c8-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="790c8-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="790c8-117">El texto del mensaje se guardará como texto con formato en formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="790c8-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="790c8-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="790c8-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="790c8-119">El texto del mensaje se guardará como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="790c8-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="790c8-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="790c8-120">_ppstm_</span></span>
  
> <span data-ttu-id="790c8-121">[salida] Puntero a un puntero a la secuencia que contendrá el mensaje guardado.</span><span class="sxs-lookup"><span data-stu-id="790c8-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="790c8-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="790c8-122">Return value</span></span>

<span data-ttu-id="790c8-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="790c8-123">S_OK</span></span> 
  
> <span data-ttu-id="790c8-124">La secuencia se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="790c8-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="790c8-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="790c8-125">Remarks</span></span>

<span data-ttu-id="790c8-126">Los objetos de formulario llaman al método **IMAPIViewContext::GetSaveStream** para recuperar una secuencia de un objeto que implementa la **interfaz IStream** para admitir el control del verbo Guardar como en el visor de formularios.</span><span class="sxs-lookup"><span data-stu-id="790c8-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="790c8-127">El método [IMAPIForm::D oVerb,](imapiform-doverb.md) que se implementa en el servidor de formularios y al que llama el visor de formularios para invocar un verbo, no debe devolverse hasta que el mensaje se convierta completamente en el formato de texto adecuado y se coloque en la secuencia adecuada.</span><span class="sxs-lookup"><span data-stu-id="790c8-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="790c8-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="790c8-128">Notes to callers</span></span>

<span data-ttu-id="790c8-129">No escriba en la secuencia a la que apunta  _ppstm antes_ de llamar **a GetSaveStream**.</span><span class="sxs-lookup"><span data-stu-id="790c8-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="790c8-130">Cuando **getSaveStream** vuelva, no restablezca la posición del puntero de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="790c8-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="790c8-131">Este puntero debe permanecer al final del texto del mensaje guardado.</span><span class="sxs-lookup"><span data-stu-id="790c8-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="790c8-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="790c8-132">See also</span></span>



[<span data-ttu-id="790c8-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="790c8-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

