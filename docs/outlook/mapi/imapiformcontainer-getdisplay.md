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
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329431"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="e2203-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="e2203-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="e2203-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e2203-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e2203-105">Devuelve el nombre para mostrar de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="e2203-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="e2203-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e2203-106">Parameters</span></span>

 <span data-ttu-id="e2203-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e2203-107">_ulFlags_</span></span>
  
> <span data-ttu-id="e2203-108">a Máscara de máscara de marcadores que controla el tipo de la cadena devuelta.</span><span class="sxs-lookup"><span data-stu-id="e2203-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="e2203-109">Se puede establecer la siguiente marca:</span><span class="sxs-lookup"><span data-stu-id="e2203-109">The following flag can be set:</span></span>
    
<span data-ttu-id="e2203-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e2203-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="e2203-111">La cadena devuelta está en formato Unicode.</span><span class="sxs-lookup"><span data-stu-id="e2203-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="e2203-112">Si no se establece la marca MAPI_UNICODE, la cadena está en formato ANSI.</span><span class="sxs-lookup"><span data-stu-id="e2203-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="e2203-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="e2203-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="e2203-114">contempla Un puntero a una cadena que contiene el nombre para mostrar del contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="e2203-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e2203-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="e2203-115">Return value</span></span>

<span data-ttu-id="e2203-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="e2203-116">S_OK</span></span> 
  
> <span data-ttu-id="e2203-117">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="e2203-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="e2203-118">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="e2203-118">MFCMAPI reference</span></span>

<span data-ttu-id="e2203-119">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="e2203-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="e2203-120">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="e2203-120">**File**</span></span>|<span data-ttu-id="e2203-121">**Función**</span><span class="sxs-lookup"><span data-stu-id="e2203-121">**Function**</span></span>|<span data-ttu-id="e2203-122">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="e2203-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="e2203-123">FormContainerDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="e2203-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="e2203-124">CFormContainerDlg:: CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="e2203-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="e2203-125">MFCMAPI usa el método **IMAPIFormContainer:: GetDisplay** para obtener el nombre del contenedor de formulario cuando representa CFormContainerDlg.</span><span class="sxs-lookup"><span data-stu-id="e2203-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2203-126">Vea también</span><span class="sxs-lookup"><span data-stu-id="e2203-126">See also</span></span>



[<span data-ttu-id="e2203-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e2203-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="e2203-128">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="e2203-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

