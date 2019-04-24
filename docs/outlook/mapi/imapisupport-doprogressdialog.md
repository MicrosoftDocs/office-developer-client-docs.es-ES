---
title: IMAPISupportDoProgressDialog
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.DoProgressDialog
api_type:
- COM
ms.assetid: 74c52b96-e903-444b-8bda-73a08f278c22
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 3de29e9af5caa82d2e57c8fcbbdab7d5ddb19dd9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32285209"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="3fe37-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="3fe37-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="3fe37-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3fe37-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3fe37-105">Recupera un objeto Progress que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="3fe37-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="3fe37-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="3fe37-106">Parameters</span></span>

 <span data-ttu-id="3fe37-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="3fe37-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="3fe37-108">a Identificador de la ventana primaria del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="3fe37-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="3fe37-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="3fe37-109">_ulFlags_</span></span>
  
> <span data-ttu-id="3fe37-110">a Máscara de máscara de marcadores que controla cómo el objeto de progreso debe calcular el progreso.</span><span class="sxs-lookup"><span data-stu-id="3fe37-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="3fe37-111">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="3fe37-111">The following flag can be set:</span></span>
    
<span data-ttu-id="3fe37-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="3fe37-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="3fe37-113">El progreso se calcula para un elemento de nivel superior, como una carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="3fe37-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="3fe37-114">El objeto Progress debe usar los valores de los parámetros _ulCount_ y _UlTotal_ del método [método imapiprogress::P rogress](imapiprogress-progress.md) , que indican el elemento actual y el total de los elementos de la operación, respectivamente, para incrementar el progreso. indicador de la operación.</span><span class="sxs-lookup"><span data-stu-id="3fe37-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="3fe37-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="3fe37-115">_lppProgress_</span></span>
  
> <span data-ttu-id="3fe37-116">contempla Un puntero a un puntero al objeto Progress.</span><span class="sxs-lookup"><span data-stu-id="3fe37-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="3fe37-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="3fe37-117">Return value</span></span>

<span data-ttu-id="3fe37-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="3fe37-118">S_OK</span></span> 
  
> <span data-ttu-id="3fe37-119">El objeto de progreso se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="3fe37-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="3fe37-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="3fe37-120">Remarks</span></span>

<span data-ttu-id="3fe37-121">El método **IMAPISupport::D oprogressdialog** se implementa para los objetos de compatibilidad de la libreta de direcciones y del proveedor de almacenamiento de mensajes.</span><span class="sxs-lookup"><span data-stu-id="3fe37-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="3fe37-122">Estos proveedores llaman a **DoProgressDialog** para obtener acceso a la implementación MAPI de la interfaz [método imapiprogress](imapiprogressiunknown.md) , que calcula la información de progreso y muestra un cuadro de diálogo estándar.</span><span class="sxs-lookup"><span data-stu-id="3fe37-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="3fe37-123">Para obtener información sobre cómo usar un objeto de progreso y la interfaz **método imapiprogress** , vea [Mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="3fe37-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="3fe37-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="3fe37-124">See also</span></span>



[<span data-ttu-id="3fe37-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3fe37-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="3fe37-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="3fe37-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="3fe37-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="3fe37-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="3fe37-128">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="3fe37-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

