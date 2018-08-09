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
ms.openlocfilehash: 527a7bb3201a4a6b1bc0807136bc88b80c189de2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817506"
---
# <a name="imapisupportdoprogressdialog"></a><span data-ttu-id="8480c-103">IMAPISupport::DoProgressDialog</span><span class="sxs-lookup"><span data-stu-id="8480c-103">IMAPISupport::DoProgressDialog</span></span>

  
  
<span data-ttu-id="8480c-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8480c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8480c-105">Recupera un objeto de progreso que muestra un indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="8480c-105">Retrieves a progress object that displays a progress indicator.</span></span>
  
```cpp
HRESULT DoProgressDialog(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIPROGRESS FAR * lppProgress
);
```

## <a name="parameters"></a><span data-ttu-id="8480c-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="8480c-106">Parameters</span></span>

 <span data-ttu-id="8480c-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="8480c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="8480c-108">[entrada] Identificador de la ventana principal del indicador de progreso.</span><span class="sxs-lookup"><span data-stu-id="8480c-108">[in] A handle to the parent window of the progress indicator.</span></span>
    
 <span data-ttu-id="8480c-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8480c-109">_ulFlags_</span></span>
  
> <span data-ttu-id="8480c-110">[entrada] Una máscara de bits de indicadores que controla cómo el objeto de progreso debe calcular el progreso.</span><span class="sxs-lookup"><span data-stu-id="8480c-110">[in] A bitmask of flags that controls how the progress object should calculate progress.</span></span> <span data-ttu-id="8480c-111">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="8480c-111">The following flag can be set:</span></span>
    
<span data-ttu-id="8480c-112">MAPI_TOP_LEVEL</span><span class="sxs-lookup"><span data-stu-id="8480c-112">MAPI_TOP_LEVEL</span></span> 
  
> <span data-ttu-id="8480c-113">Progreso se calcula para un elemento de nivel superior, como una carpeta principal.</span><span class="sxs-lookup"><span data-stu-id="8480c-113">Progress is calculated for a top-level item, such as a parent folder.</span></span> <span data-ttu-id="8480c-114">El objeto de progreso debe utilizar los valores de parámetros de _ulCount_ y _ulTotal_ del método [IMAPIProgress::Progress](imapiprogress-progress.md) , que indican el elemento actual y los elementos totales en la operación, respectivamente, para incrementar el progreso indicador para la operación.</span><span class="sxs-lookup"><span data-stu-id="8480c-114">The progress object should use the values in the [IMAPIProgress::Progress](imapiprogress-progress.md) method's  _ulCount_ and  _ulTotal_ parameters — which indicate the current item and the total items in the operation, respectively — to increment the progress indicator for the operation.</span></span> 
    
 <span data-ttu-id="8480c-115">_lppProgress_</span><span class="sxs-lookup"><span data-stu-id="8480c-115">_lppProgress_</span></span>
  
> <span data-ttu-id="8480c-116">[out] Un puntero a un puntero al objeto de progreso.</span><span class="sxs-lookup"><span data-stu-id="8480c-116">[out] A pointer to a pointer to the progress object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8480c-117">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8480c-117">Return value</span></span>

<span data-ttu-id="8480c-118">S_OK</span><span class="sxs-lookup"><span data-stu-id="8480c-118">S_OK</span></span> 
  
> <span data-ttu-id="8480c-119">El objeto de progreso se recuperó correctamente.</span><span class="sxs-lookup"><span data-stu-id="8480c-119">The progress object was successfully retrieved.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8480c-120">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8480c-120">Remarks</span></span>

<span data-ttu-id="8480c-121">El método **IMAPISupport::DoProgressDialog** se implementa para dirección libreta de direcciones y el mensaje de proveedor compatibilidad con objetos de almacén.</span><span class="sxs-lookup"><span data-stu-id="8480c-121">The **IMAPISupport::DoProgressDialog** method is implemented for address book and message store provider support objects.</span></span> <span data-ttu-id="8480c-122">Estos proveedores de llamar a **DoProgressDialog** para obtener acceso a la implementación de la interfaz [IMAPIProgress](imapiprogressiunknown.md) , que calcula la información de progreso y muestra un cuadro de diálogo estándar de MAPI.</span><span class="sxs-lookup"><span data-stu-id="8480c-122">These providers call **DoProgressDialog** to access the MAPI implementation of the [IMAPIProgress](imapiprogressiunknown.md) interface, which calculates the progress information and displays a standard dialog box.</span></span> 
  
<span data-ttu-id="8480c-123">Para obtener información acerca de cómo usar un objeto de progreso y la interfaz de **IMAPIProgress** , consulte [para mostrar un indicador de progreso](how-to-display-a-progress-indicator.md).</span><span class="sxs-lookup"><span data-stu-id="8480c-123">For information about how to use a progress object and the **IMAPIProgress** interface, see [Display a Progress Indicator](how-to-display-a-progress-indicator.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="8480c-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="8480c-124">See also</span></span>



[<span data-ttu-id="8480c-125">IMAPIProgress : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8480c-125">IMAPIProgress : IUnknown</span></span>](imapiprogressiunknown.md)
  
[<span data-ttu-id="8480c-126">IMAPIProgress::Progress</span><span class="sxs-lookup"><span data-stu-id="8480c-126">IMAPIProgress::Progress</span></span>](imapiprogress-progress.md)
  
[<span data-ttu-id="8480c-127">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="8480c-127">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="8480c-128">Mostrar un indicador de progreso</span><span class="sxs-lookup"><span data-stu-id="8480c-128">Display a Progress Indicator</span></span>](how-to-display-a-progress-indicator.md)

