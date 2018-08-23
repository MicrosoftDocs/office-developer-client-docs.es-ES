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
ms.openlocfilehash: 1a1d11db538d9b5368d80962e44b9eab38b490d2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575654"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="19076-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="19076-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="19076-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19076-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19076-105">Quita un formulario en particular de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="19076-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="19076-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="19076-106">Parameters</span></span>

 <span data-ttu-id="19076-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="19076-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="19076-108">[entrada] Una cadena que da nombre a la clase de mensaje del formulario que se quitará del contenedor del formulario.</span><span class="sxs-lookup"><span data-stu-id="19076-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="19076-109">Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="19076-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="19076-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="19076-110">Return value</span></span>

<span data-ttu-id="19076-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="19076-111">S_OK</span></span> 
  
> <span data-ttu-id="19076-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="19076-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="19076-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="19076-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="19076-114">La clase de mensaje que se pasa en el parámetro _szMessageClass_ no coincide con la clase de mensaje de cualquier formulario en el contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="19076-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="19076-115">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="19076-115">MFCMAPI reference</span></span>

<span data-ttu-id="19076-116">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="19076-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="19076-117">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="19076-117">**File**</span></span>|<span data-ttu-id="19076-118">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="19076-118">**Function**</span></span>|<span data-ttu-id="19076-119">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="19076-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="19076-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="19076-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="19076-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="19076-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="19076-122">MFCMAPI usa el método **IMAPIFormContainer::RemoveForm** para eliminar un formulario de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="19076-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="19076-123">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="19076-123">See also</span></span>



[<span data-ttu-id="19076-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="19076-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="19076-125">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="19076-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

