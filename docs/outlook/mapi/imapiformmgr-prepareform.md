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
description: '�ltima modificaci�n: s�bado, 23 de julio de 2011'
ms.openlocfilehash: 3b10ac5906be0f95930be3bef51fe2d78d583b03
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817326"
---
# <a name="imapiformmgrprepareform"></a><span data-ttu-id="48085-103">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="48085-103">IMAPIFormMgr::PrepareForm</span></span>

  
  
<span data-ttu-id="48085-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48085-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48085-105">Descargas de un formulario para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="48085-105">Downloads a form for opening.</span></span>
  
```cpp
HRESULT PrepareForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMINFO pfrmiInfo
);
```

## <a name="parameters"></a><span data-ttu-id="48085-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="48085-106">Parameters</span></span>

 <span data-ttu-id="48085-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="48085-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="48085-108">[entrada] Identificador de la ventana principal del indicador de progreso que se muestra mientras se descarga el formulario.</span><span class="sxs-lookup"><span data-stu-id="48085-108">[in] A handle to the parent window of the progress indicator that is displayed while the form is downloaded.</span></span> <span data-ttu-id="48085-109">El parámetro _ulUIParam_ se omite a menos que la marca MAPI_DIALOG se establece en el parámetro _ulFlags indicado_ .</span><span class="sxs-lookup"><span data-stu-id="48085-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="48085-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="48085-110">_ulFlags_</span></span>
  
> <span data-ttu-id="48085-111">[entrada] Una máscara de bits de indicadores que controla cómo se descarga el formulario.</span><span class="sxs-lookup"><span data-stu-id="48085-111">[in] A bitmask of flags that controls how the form is downloaded.</span></span> <span data-ttu-id="48085-112">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="48085-112">The following flag can be set:</span></span>
    
<span data-ttu-id="48085-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="48085-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="48085-114">Muestra una interfaz de usuario para proporcionar el estado o solicite al usuario para obtener más información.</span><span class="sxs-lookup"><span data-stu-id="48085-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="48085-115">Si no se establece este marcador, no se muestra ninguna interfaz de usuario.</span><span class="sxs-lookup"><span data-stu-id="48085-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="48085-116">_pfrmiInfo_</span><span class="sxs-lookup"><span data-stu-id="48085-116">_pfrmiInfo_</span></span>
  
> <span data-ttu-id="48085-117">[entrada] Un puntero a un objeto de información de formulario para el formulario que se va a descargar.</span><span class="sxs-lookup"><span data-stu-id="48085-117">[in] A pointer to a form information object for the form to be downloaded.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="48085-118">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48085-118">Return value</span></span>

<span data-ttu-id="48085-119">S_OK</span><span class="sxs-lookup"><span data-stu-id="48085-119">S_OK</span></span> 
  
> <span data-ttu-id="48085-120">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="48085-120">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48085-121">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48085-121">Remarks</span></span>

<span data-ttu-id="48085-122">Visores de formulario llamar al método **IMAPIFormMgr::PrepareForm** para descargar un formulario desde un contenedor de formulario para abrirlo.</span><span class="sxs-lookup"><span data-stu-id="48085-122">Form viewers call the **IMAPIFormMgr::PrepareForm** method to download a form from a form container for opening.</span></span> <span data-ttu-id="48085-123">La mayoría de los visores de formulario no es necesario llamar a **PrepareForm**, debido a que la [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) y el [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) métodos llaman **PrepareForm**, si es necesario.</span><span class="sxs-lookup"><span data-stu-id="48085-123">Most form viewers do not need to call **PrepareForm**, because both the [IMAPIFormMgr::CreateForm](imapiformmgr-createform.md) and [IMAPIFormMgr::LoadForm](imapiformmgr-loadform.md) methods call **PrepareForm**, if necessary.</span></span> 
  
<span data-ttu-id="48085-124">Puede usar **PrepareForm** para obtener las bibliotecas de vínculos dinámicos (DLL) y otros archivos asociados con un formulario para modificarlos.</span><span class="sxs-lookup"><span data-stu-id="48085-124">You can use **PrepareForm** to obtain the dynamic-link libraries (DLLs) and other files associated with a form to modify them.</span></span> <span data-ttu-id="48085-125">Si se carga el formulario modificado en su contenedor de formulario, se debe volver a instalar.</span><span class="sxs-lookup"><span data-stu-id="48085-125">If the modified form is loaded back into its form container, it must be reinstalled.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48085-126">Ver también</span><span class="sxs-lookup"><span data-stu-id="48085-126">See also</span></span>



[<span data-ttu-id="48085-127">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="48085-127">IMAPIFormMgr::CreateForm</span></span>](imapiformmgr-createform.md)
  
[<span data-ttu-id="48085-128">IMAPIFormMgr::LoadForm</span><span class="sxs-lookup"><span data-stu-id="48085-128">IMAPIFormMgr::LoadForm</span></span>](imapiformmgr-loadform.md)
  
[<span data-ttu-id="48085-129">IMAPIFormMgr: IUnknown</span><span class="sxs-lookup"><span data-stu-id="48085-129">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

