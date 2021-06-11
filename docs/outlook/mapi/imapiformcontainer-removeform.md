---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: e53c0cbd9946ff04516594a7ce99fdc2daf4ff4d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432201"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="2ab94-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="2ab94-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="2ab94-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ab94-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ab94-105">Quita un formulario determinado de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="2ab94-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="2ab94-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="2ab94-106">Parameters</span></span>

 <span data-ttu-id="2ab94-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="2ab94-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="2ab94-108">[in] Cadena que nombra la clase de mensaje del formulario que se va a quitar del contenedor del formulario.</span><span class="sxs-lookup"><span data-stu-id="2ab94-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="2ab94-109">Los nombres de clase de mensaje siempre son cadenas ANSI, nunca Unicode.</span><span class="sxs-lookup"><span data-stu-id="2ab94-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2ab94-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="2ab94-110">Return value</span></span>

<span data-ttu-id="2ab94-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="2ab94-111">S_OK</span></span> 
  
> <span data-ttu-id="2ab94-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="2ab94-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="2ab94-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="2ab94-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="2ab94-114">La clase de mensaje pasada en  _el parámetro szMessageClass_ no coincide con la clase de mensaje de ningún formulario del contenedor del formulario.</span><span class="sxs-lookup"><span data-stu-id="2ab94-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2ab94-115">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2ab94-115">MFCMAPI reference</span></span>

<span data-ttu-id="2ab94-116">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="2ab94-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2ab94-117">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="2ab94-117">**File**</span></span>|<span data-ttu-id="2ab94-118">**Función**</span><span class="sxs-lookup"><span data-stu-id="2ab94-118">**Function**</span></span>|<span data-ttu-id="2ab94-119">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="2ab94-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2ab94-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2ab94-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="2ab94-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="2ab94-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="2ab94-122">MFCMAPI usa el **método IMAPIFormContainer::RemoveForm** para eliminar un formulario de un contenedor de formularios.</span><span class="sxs-lookup"><span data-stu-id="2ab94-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2ab94-123">Vea también</span><span class="sxs-lookup"><span data-stu-id="2ab94-123">See also</span></span>



[<span data-ttu-id="2ab94-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2ab94-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="2ab94-125">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="2ab94-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

