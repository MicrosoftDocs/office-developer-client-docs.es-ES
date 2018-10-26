---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 66e23d73af53b05295bf2cbcd8c604ab3545bbca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573141"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="6bb06-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="6bb06-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="6bb06-104">**Hace referencia a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bb06-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bb06-105">Devuelve el nombre para mostrar de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="6bb06-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="6bb06-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="6bb06-106">Parameters</span></span>

 <span data-ttu-id="6bb06-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="6bb06-107">_ulFlags_</span></span>
  
> <span data-ttu-id="6bb06-108">[entrada] Una máscara de bits de indicadores que controla el tipo de la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="6bb06-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="6bb06-109">Se puede establecer la marca siguiente:</span><span class="sxs-lookup"><span data-stu-id="6bb06-109">The following flag can be set:</span></span>
    
<span data-ttu-id="6bb06-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6bb06-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="6bb06-111">La cadena devuelta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="6bb06-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="6bb06-112">Si no está establecido el indicador MAPI_UNICODE., la cadena está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="6bb06-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="6bb06-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="6bb06-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="6bb06-114">[out] Un puntero a una cadena que contiene el nombre para mostrar del contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="6bb06-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6bb06-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="6bb06-115">Return value</span></span>

<span data-ttu-id="6bb06-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="6bb06-116">S_OK</span></span> 
  
> <span data-ttu-id="6bb06-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="6bb06-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="6bb06-118">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6bb06-118">MFCMAPI reference</span></span>

<span data-ttu-id="6bb06-119">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="6bb06-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6bb06-120">**File**</span><span class="sxs-lookup"><span data-stu-id="6bb06-120">**File**</span></span>|<span data-ttu-id="6bb06-121">**Función**</span><span class="sxs-lookup"><span data-stu-id="6bb06-121">**Function**</span></span>|<span data-ttu-id="6bb06-122">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="6bb06-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6bb06-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6bb06-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="6bb06-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="6bb06-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="6bb06-125">MFCMAPI usa el método **IMAPIFormContainer::GetDisplay** para obtener el nombre del contenedor de formulario cuando se representa CFormContainerDlg.</span><span class="sxs-lookup"><span data-stu-id="6bb06-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6bb06-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="6bb06-126">See also</span></span>



[<span data-ttu-id="6bb06-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6bb06-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="6bb06-128">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="6bb06-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

