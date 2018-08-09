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
ms.openlocfilehash: 7981dc8550485aa22859c4a8dc25541bedf1217c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817633"
---
# <a name="imapiviewcontextgetsavestream"></a><span data-ttu-id="677b0-103">IMAPIViewContext::GetSaveStream</span><span class="sxs-lookup"><span data-stu-id="677b0-103">IMAPIViewContext::GetSaveStream</span></span>

  
  
<span data-ttu-id="677b0-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="677b0-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="677b0-105">Recupera una secuencia que se utilizará para guardar el mensaje actual.</span><span class="sxs-lookup"><span data-stu-id="677b0-105">Retrieves a stream to be used for saving the current message.</span></span>
  
```cpp
HRESULT GetSaveStream(
ULONG FAR * pulFlags,
ULONG FAR * pulFormat,
LPSTREAM FAR * ppstm
);
```

## <a name="parameters"></a><span data-ttu-id="677b0-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="677b0-106">Parameters</span></span>

 <span data-ttu-id="677b0-107">_pulFlags_</span><span class="sxs-lookup"><span data-stu-id="677b0-107">_pulFlags_</span></span>
  
> <span data-ttu-id="677b0-108">[out] Puntero a una máscara de bits de indicadores que controla cómo se debe guardar el texto del mensaje.</span><span class="sxs-lookup"><span data-stu-id="677b0-108">[out] Pointer to a bitmask of flags that controls how the message text should be saved.</span></span> <span data-ttu-id="677b0-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="677b0-109">The following flag can be set:</span></span>
    
<span data-ttu-id="677b0-110">MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="677b0-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="677b0-111">El texto del mensaje se guarda en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="677b0-111">The message text is saved in Unicode format.</span></span> <span data-ttu-id="677b0-112">Si no está establecido el indicador MAPI_UNICODE., el texto se guarda en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="677b0-112">If the MAPI_UNICODE flag is not set, the text is saved in ANSI format.</span></span>
    
 <span data-ttu-id="677b0-113">_pulFormat_</span><span class="sxs-lookup"><span data-stu-id="677b0-113">_pulFormat_</span></span>
  
> <span data-ttu-id="677b0-114">[out] Puntero a una máscara de bits de indicadores que controla el formato del texto guardado.</span><span class="sxs-lookup"><span data-stu-id="677b0-114">[out] Pointer to a bitmask of flags that controls the format of the saved text.</span></span> <span data-ttu-id="677b0-115">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="677b0-115">The following flags can be set:</span></span>
    
<span data-ttu-id="677b0-116">SAVE_FORMAT_RICHTEXT</span><span class="sxs-lookup"><span data-stu-id="677b0-116">SAVE_FORMAT_RICHTEXT</span></span> 
  
> <span data-ttu-id="677b0-117">El texto del mensaje es que se guarde como texto con formato en el formato de texto enriquecido (RTF).</span><span class="sxs-lookup"><span data-stu-id="677b0-117">The message text is to be saved as formatted text in the Rich Text Format (RTF).</span></span> 
    
<span data-ttu-id="677b0-118">SAVE_FORMAT_TEXT</span><span class="sxs-lookup"><span data-stu-id="677b0-118">SAVE_FORMAT_TEXT</span></span> 
  
> <span data-ttu-id="677b0-119">El texto del mensaje es que se guarde como texto sin formato.</span><span class="sxs-lookup"><span data-stu-id="677b0-119">The message text is to be saved as plain text.</span></span> 
    
 <span data-ttu-id="677b0-120">_ppstm_</span><span class="sxs-lookup"><span data-stu-id="677b0-120">_ppstm_</span></span>
  
> <span data-ttu-id="677b0-121">[out] Puntero a un puntero a la secuencia que va a contener el mensaje guardado.</span><span class="sxs-lookup"><span data-stu-id="677b0-121">[out] Pointer to a pointer to the stream that will contain the saved message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="677b0-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="677b0-122">Return value</span></span>

<span data-ttu-id="677b0-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="677b0-123">S_OK</span></span> 
  
> <span data-ttu-id="677b0-124">La secuencia se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="677b0-124">The stream was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="677b0-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="677b0-125">Remarks</span></span>

<span data-ttu-id="677b0-126">Objetos de formulario llamar al método **IMAPIViewContext::GetSaveStream** para recuperar una secuencia de un objeto que implementa la interfaz **IStream** para admitir la administración del verbo Guardar como en el Visor de formulario.</span><span class="sxs-lookup"><span data-stu-id="677b0-126">Form objects call the **IMAPIViewContext::GetSaveStream** method to retrieve a stream an object that implements the **IStream** interface to support the handling of the Save As verb in the form viewer.</span></span> <span data-ttu-id="677b0-127">El método [IMAPIForm::DoVerb](imapiform-doverb.md) , que se implementa en el servidor de formulario y llamado por el Visor de formulario para invocar un verbo, no debe devolver hasta que el mensaje se convierte en el formato de texto adecuado y se coloca en la secuencia adecuada totalmente.</span><span class="sxs-lookup"><span data-stu-id="677b0-127">The [IMAPIForm::DoVerb](imapiform-doverb.md) method, which is implemented in the form server and called by the form viewer to invoke a verb, should not return until the message is fully converted into the appropriate text format and placed into the appropriate stream.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="677b0-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="677b0-128">Notes to callers</span></span>

<span data-ttu-id="677b0-129">No se puede escribir en la secuencia indicada por _ppstm_ antes de llamar a **GetSaveStream**.</span><span class="sxs-lookup"><span data-stu-id="677b0-129">Do not write to the stream pointed to by  _ppstm_ before calling **GetSaveStream**.</span></span> <span data-ttu-id="677b0-130">Cuando se devuelve **GetSaveStream** , no restablezca la posición del puntero de búsqueda.</span><span class="sxs-lookup"><span data-stu-id="677b0-130">When **GetSaveStream** returns, do not reset the position of the seek pointer.</span></span> <span data-ttu-id="677b0-131">Este puntero debe permanecer al final del texto del mensaje guardado.</span><span class="sxs-lookup"><span data-stu-id="677b0-131">This pointer must remain at the end of the saved message text.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="677b0-132">Vea también</span><span class="sxs-lookup"><span data-stu-id="677b0-132">See also</span></span>



[<span data-ttu-id="677b0-133">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="677b0-133">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)

