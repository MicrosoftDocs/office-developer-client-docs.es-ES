---
title: IMAPIViewAdviseSinkOnPrint
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewAdviseSink.OnPrint
api_type:
- COM
ms.assetid: d16219a0-268c-428d-9f02-4f06eb5b6d7d
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: bf3eee43a70fbc4abf32b60379fc7b191bd9d513
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817612"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="eb3aa-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="eb3aa-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="eb3aa-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="eb3aa-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="eb3aa-105">Se notifica el Visor de formulario del estado de impresión de un formulario.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="eb3aa-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="eb3aa-106">Parameters</span></span>

 <span data-ttu-id="eb3aa-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="eb3aa-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="eb3aa-108">[entrada] Imprime el número de la última página.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="eb3aa-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="eb3aa-109">_hrStatus_</span></span>
  
> <span data-ttu-id="eb3aa-110">[entrada] Valor HRESULT que indica el estado del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="eb3aa-111">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="eb3aa-111">Possible values are:</span></span>
    
<span data-ttu-id="eb3aa-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="eb3aa-112">S_FALSE</span></span> 
  
> <span data-ttu-id="eb3aa-113">El trabajo de impresión se completó satisfactoriamente.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="eb3aa-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb3aa-114">S_OK</span></span> 
  
> <span data-ttu-id="eb3aa-115">El trabajo de impresión está en curso.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="eb3aa-116">NO SE PUDO</span><span class="sxs-lookup"><span data-stu-id="eb3aa-116">FAILED</span></span> 
  
> <span data-ttu-id="eb3aa-117">El trabajo de impresión se ha terminado debido a un error.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="eb3aa-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="eb3aa-118">Return value</span></span>

<span data-ttu-id="eb3aa-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="eb3aa-119">S_OK</span></span> 
  
> <span data-ttu-id="eb3aa-120">La notificación se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-120">The notification succeeded.</span></span>
    
<span data-ttu-id="eb3aa-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="eb3aa-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="eb3aa-122">El usuario canceló la operación, normalmente haciendo clic en el botón Cancelar en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="eb3aa-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="eb3aa-123">Remarks</span></span>

<span data-ttu-id="eb3aa-124">Objetos de formulario llamar al método **IMAPIViewAdviseSink::OnPrint** durante la impresión para notificar al Visor de progreso de la impresión.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="eb3aa-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="eb3aa-125">Notes to callers</span></span>

<span data-ttu-id="eb3aa-126">Si el trabajo de impresión implica varias páginas, puede llamar a **OnPrint** después de cada página se imprime.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="eb3aa-127">Establezca _dwPageNumber_ a la página que actualmente se está imprimiendo y _hrStatus_ en S_OK.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="eb3aa-128">Una vez completado el trabajo de impresión, llame al que conjunto de **OnPrint** con _dwPageNumber_ a la última página impresa y _hrStatus_ se establecen en S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="eb3aa-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="eb3aa-129">Para obtener más información acerca de las notificaciones de formulario, vea [Enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="eb3aa-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="eb3aa-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="eb3aa-130">See also</span></span>



[<span data-ttu-id="eb3aa-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="eb3aa-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

