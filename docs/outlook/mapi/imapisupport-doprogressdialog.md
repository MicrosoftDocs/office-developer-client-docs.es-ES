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
ms.openlocfilehash: 32174e213334d784220b960364443e60db6d1d19
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582780"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="22835-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="22835-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="22835-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22835-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22835-105">Recupera un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="22835-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="22835-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="22835-106">Parameters</span></span>

 <span data-ttu-id="22835-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="22835-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="22835-108">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="22835-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="22835-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="22835-109">_ulFlags_</span></span>
  
> <span data-ttu-id="22835-110">[entrada] Una máscara de bits de indicadores que controla cómo el objeto de progreso debe calcular el progreso.</span><span class="sxs-lookup"><span data-stu-id="22835-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="22835-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="22835-111">The following flag can be set:</span></span>
    
<span data-ttu-id="22835-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="22835-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="22835-113">Progreso se calcula para un elemento de nivel superior, como una carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="22835-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="22835-114">El objeto de progreso debe utilizar los valores de parámetros de _ulCount_ y _ulTotal_ del método [IMAPIProgress::Progress](imapiprogress-progress.md) , que indican el elemento actual y los elementos totales en la operación, respectivamente, para incrementar el progreso indicador para la operación.</span><span class="sxs-lookup"><span data-stu-id="22835-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="22835-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="22835-115">_lppProgress_</span></span>
  
> <span data-ttu-id="22835-116">[out] Un puntero a un puntero al objeto de progreso.</span><span class="sxs-lookup"><span data-stu-id="22835-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="22835-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="22835-117">Return value</span></span>

<span data-ttu-id="22835-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="22835-118">S_OK</span></span> 
  
> <span data-ttu-id="22835-119">El objeto de progreso se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="22835-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="22835-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="22835-120">Remarks</span></span>

<span data-ttu-id="22835-121">El método **IMAPISupport::DoProgressDialog** se implementa para dirección libreta de direcciones y el mensaje de proveedor compatibilidad con objetos de almacén.</span><span class="sxs-lookup"><span data-stu-id="22835-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="22835-122">Estos proveedores de llamar a **DoProgressDialog** para obtener acceso a la implementación de la interfaz [IMAPIProgress](imapiprogressiunknown.md) , que calcula la información de progreso y muestra un cuadro de diálogo estándar de MAPI.</span><span class="sxs-lookup"><span data-stu-id="22835-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="22835-123">Para obtener información acerca de cómo usar un objeto de progreso y la interfaz de **IMAPIProgress** , consulte [para mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="22835-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="22835-124">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="22835-124">See also</span></span>



[<span data-ttu-id="22835-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="22835-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="22835-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="22835-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="22835-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="22835-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="22835-128">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="22835-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

