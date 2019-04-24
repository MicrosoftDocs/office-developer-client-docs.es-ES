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
ms.openlocfilehash: e66315042f8b5cd5aff0e4aa076588c9f312376a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328787"
---
# <a name="imapiviewadvisesinkonprint"></a><span data-ttu-id="a9261-103">IMAPIViewAdviseSink::OnPrint</span><span class="sxs-lookup"><span data-stu-id="a9261-103">IMAPIViewAdviseSink::OnPrint</span></span>

  
  
<span data-ttu-id="a9261-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a9261-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a9261-105">Notifica al visor del formulario el estado de impresión de un formulario.</span><span class="sxs-lookup"><span data-stu-id="a9261-105">Notifies the form viewer of the printing status of a form.</span></span>
  
```cpp
HRESULT OnPrint(
ULONG dwPageNumber,
HRESULT hrStatus
);
```

## <a name="parameters"></a><span data-ttu-id="a9261-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="a9261-106">Parameters</span></span>

 <span data-ttu-id="a9261-107">_dwPageNumber_</span><span class="sxs-lookup"><span data-stu-id="a9261-107">_dwPageNumber_</span></span>
  
> <span data-ttu-id="a9261-108">a Número de la última página impresa.</span><span class="sxs-lookup"><span data-stu-id="a9261-108">[in] Number of the last page printed.</span></span>
    
 <span data-ttu-id="a9261-109">_hrStatus_</span><span class="sxs-lookup"><span data-stu-id="a9261-109">_hrStatus_</span></span>
  
> <span data-ttu-id="a9261-110">a Valor HRESULT que indica el estado del trabajo de impresión.</span><span class="sxs-lookup"><span data-stu-id="a9261-110">[in] An HRESULT value indicating the status of the print job.</span></span> <span data-ttu-id="a9261-111">Los valores posibles son:</span><span class="sxs-lookup"><span data-stu-id="a9261-111">Possible values are:</span></span>
    
<span data-ttu-id="a9261-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="a9261-112">S_FALSE</span></span> 
  
> <span data-ttu-id="a9261-113">El trabajo de impresión ha finalizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="a9261-113">The printing job has finished successfully.</span></span>
    
<span data-ttu-id="a9261-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9261-114">S_OK</span></span> 
  
> <span data-ttu-id="a9261-115">El trabajo de impresión está en curso.</span><span class="sxs-lookup"><span data-stu-id="a9261-115">The printing job is in progress.</span></span>
    
<span data-ttu-id="a9261-116">ERRÓNEA</span><span class="sxs-lookup"><span data-stu-id="a9261-116">FAILED</span></span> 
  
> <span data-ttu-id="a9261-117">El trabajo de impresión se terminó debido a un error.</span><span class="sxs-lookup"><span data-stu-id="a9261-117">The printing job was terminated due to a failure.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a9261-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="a9261-118">Return value</span></span>

<span data-ttu-id="a9261-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="a9261-119">S_OK</span></span> 
  
> <span data-ttu-id="a9261-120">La notificación se realizó correctamente.</span><span class="sxs-lookup"><span data-stu-id="a9261-120">The notification succeeded.</span></span>
    
<span data-ttu-id="a9261-121">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a9261-121">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a9261-122">El usuario canceló la operación, normalmente haciendo clic en el botón Cancelar en un cuadro de diálogo.</span><span class="sxs-lookup"><span data-stu-id="a9261-122">The user canceled the operation, typically by clicking the Cancel button in a dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a9261-123">Comentarios</span><span class="sxs-lookup"><span data-stu-id="a9261-123">Remarks</span></span>

<span data-ttu-id="a9261-124">Los objetos de formulario llaman al método **IMAPIViewAdviseSink:: OnPrint** durante la impresión para informar al usuario sobre el progreso de la impresión.</span><span class="sxs-lookup"><span data-stu-id="a9261-124">Form objects call the **IMAPIViewAdviseSink::OnPrint** method while printing to inform the viewer of printing progress.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="a9261-125">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="a9261-125">Notes to callers</span></span>

<span data-ttu-id="a9261-126">Si el trabajo de impresión implica varias páginas, puede llamar a **OnPrint** después de imprimir cada página.</span><span class="sxs-lookup"><span data-stu-id="a9261-126">If the printing job involves multiple pages, you can call **OnPrint** after each page is printed.</span></span> <span data-ttu-id="a9261-127">Establezca _dwPageNumber_ en la página que se está imprimiendo actualmente y _hrStatus_ en S_OK.</span><span class="sxs-lookup"><span data-stu-id="a9261-127">Set  _dwPageNumber_ to the page currently being printed and  _hrStatus_ to S_OK.</span></span> <span data-ttu-id="a9261-128">Una vez finalizado el trabajo de impresión, llame a **OnPrint** con _dwPageNumber_ establecido en la última página impresa y _hrStatus_ establecido en S_FALSE.</span><span class="sxs-lookup"><span data-stu-id="a9261-128">When the printing job is complete, call **OnPrint** with  _dwPageNumber_ set to the last page printed and  _hrStatus_ set to S_FALSE.</span></span> 
  
<span data-ttu-id="a9261-129">Para obtener más información acerca de las notificaciones de formulario, vea [enviar y recibir notificaciones de formulario](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="a9261-129">For more information about form notifications, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a9261-130">Vea también</span><span class="sxs-lookup"><span data-stu-id="a9261-130">See also</span></span>



[<span data-ttu-id="a9261-131">IMAPIViewAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a9261-131">IMAPIViewAdviseSink : IUnknown</span></span>](imapiviewadvisesinkiunknown.md)

