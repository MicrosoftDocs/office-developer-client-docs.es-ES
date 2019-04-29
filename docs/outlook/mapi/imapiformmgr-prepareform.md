---
title: IMAPIFormMgrPrepareForm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.PrepareForm
api_type:
- COM
ms.assetid: 8f8ee2cb-1c2a-4958-b01e-2f4aab689f89
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d0d5d8fe13a3c192dc0b0a8ddc0f5f945fa16f15
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416653"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="ac68f-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="ac68f-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="ac68f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ac68f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ac68f-105">Descarga un formulario para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="ac68f-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="ac68f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ac68f-106">Parameters</span></span>

 <span data-ttu-id="ac68f-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="ac68f-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="ac68f-108">a Identificador de la ventana primaria del indicador de progreso que se muestra mientras se descarga el formulario.</span><span class="sxs-lookup"><span data-stu-id="ac68f-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="ac68f-109">El parámetro _ulUIParam_ se omite a menos que se establezca la marca MAPI_DIALOG en el parámetro _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="ac68f-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="ac68f-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="ac68f-110">_ulFlags_</span></span>
  
> <span data-ttu-id="ac68f-111">a Máscara de máscara de marcadores que controla cómo se descarga el formulario.</span><span class="sxs-lookup"><span data-stu-id="ac68f-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="ac68f-112">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="ac68f-112">The following flag can be set:</span></span>
    
<span data-ttu-id="ac68f-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="ac68f-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="ac68f-114">Muestra una interfaz de usuario para proporcionar el estado o solicitar información al usuario.</span><span class="sxs-lookup"><span data-stu-id="ac68f-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="ac68f-115">Si no se establece esta marca, no se muestra ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="ac68f-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="ac68f-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="ac68f-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="ac68f-117">a Un puntero a un objeto de información de formulario para el formulario que se va a descargar.</span><span class="sxs-lookup"><span data-stu-id="ac68f-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ac68f-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="ac68f-118">Return value</span></span>

<span data-ttu-id="ac68f-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="ac68f-119">S_OK</span></span> 
  
> <span data-ttu-id="ac68f-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="ac68f-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ac68f-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="ac68f-121">Remarks</span></span>

<span data-ttu-id="ac68f-122">Los visores de formularios llaman al método **IMAPIFormMgr::P repareform** para descargar un formulario de un contenedor de formularios para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="ac68f-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="ac68f-123">La mayoría de los visores de formulario no necesitan llamar a **PrepareForm**, ya que los métodos [IMAPIFormMgr:: CreateForm](imapiformmgr-createform.md) y [IMAPIFormMgr:: LoadForm](imapiformmgr-loadform.md) llaman a **PrepareForm**, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="ac68f-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="ac68f-124">Puede usar **PrepareForm** para obtener las bibliotecas de vínculos dinámicos (dll) y otros archivos asociados a un formulario para modificarlas.</span><span class="sxs-lookup"><span data-stu-id="ac68f-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="ac68f-125">Si el formulario modificado se vuelve a cargar en su contenedor de formularios, se debe volver a instalar.</span><span class="sxs-lookup"><span data-stu-id="ac68f-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ac68f-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="ac68f-126">See also</span></span>



[<span data-ttu-id="ac68f-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="ac68f-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="ac68f-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="ac68f-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="ac68f-129">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ac68f-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

