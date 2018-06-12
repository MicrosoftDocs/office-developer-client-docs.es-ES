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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 0d2c908f86ccd66ffd3a2eb2506d129ee2a14d48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817273"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="259c9-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="259c9-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="259c9-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="259c9-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="259c9-105">Quita un formulario en particular de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="259c9-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="259c9-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="259c9-106">Parameters</span></span>

 <span data-ttu-id="259c9-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="259c9-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="259c9-108">[entrada] Una cadena que da nombre a la clase de mensaje del formulario que se quitará del contenedor del formulario.</span><span class="sxs-lookup"><span data-stu-id="259c9-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="259c9-109">Los nombres de clase de mensaje siempre son cadenas ANSI, Unicode nunca.</span><span class="sxs-lookup"><span data-stu-id="259c9-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="259c9-110">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="259c9-110">Return value</span></span>

<span data-ttu-id="259c9-111">S_OK</span><span class="sxs-lookup"><span data-stu-id="259c9-111">S_OK</span></span> 
  
> <span data-ttu-id="259c9-112">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="259c9-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="259c9-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="259c9-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="259c9-114">La clase de mensaje que se pasa en el parámetro _szMessageClass_ no coincide con la clase de mensaje de cualquier formulario en el contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="259c9-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="259c9-115">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="259c9-115">MFCMAPI reference</span></span>

<span data-ttu-id="259c9-116">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="259c9-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="259c9-117">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="259c9-117">**File**</span></span>|<span data-ttu-id="259c9-118">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="259c9-118">**Function**</span></span>|<span data-ttu-id="259c9-119">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="259c9-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="259c9-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="259c9-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="259c9-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="259c9-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="259c9-122">MFCMAPI usa el método **IMAPIFormContainer::RemoveForm** para eliminar un formulario de un contenedor de formulario.</span><span class="sxs-lookup"><span data-stu-id="259c9-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="259c9-123">Ver también</span><span class="sxs-lookup"><span data-stu-id="259c9-123">See also</span></span>



[<span data-ttu-id="259c9-124">IMAPIFormContainer: IUnknown</span><span class="sxs-lookup"><span data-stu-id="259c9-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="259c9-125">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="259c9-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

