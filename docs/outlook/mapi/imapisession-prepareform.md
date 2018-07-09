---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 026a120406b714a50a9191e4761021693a250b94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817450"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="222fe-103">IMAPISession:: PrepareForm</span><span class="sxs-lookup"><span data-stu-id="222fe-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="222fe-104">**Se aplica a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="222fe-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="222fe-105">Crea un token numérico que usa el método [IMAPISession:: ShowForm](imapisession-showform.md) para tener acceso a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="222fe-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="222fe-106">Sintaxis</span><span class="sxs-lookup"><span data-stu-id="222fe-106">Parameters</span></span>

 <span data-ttu-id="222fe-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="222fe-107">_lpInterface_</span></span>
  
> <span data-ttu-id="222fe-108">[entrada] Un puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al mensaje.</span><span class="sxs-lookup"><span data-stu-id="222fe-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="222fe-109">**Null** resultados satisfactorios en la interfaz estándar, o [IMessage](imessageimapiprop.md), que se usa.</span><span class="sxs-lookup"><span data-stu-id="222fe-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="222fe-110">El parámetro _lpInterface_ debe ser **nulo** o IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="222fe-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="222fe-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="222fe-111">_lpMessage_</span></span>
  
> <span data-ttu-id="222fe-112">[entrada] Un puntero al mensaje que se mostrará en el formulario.</span><span class="sxs-lookup"><span data-stu-id="222fe-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="222fe-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="222fe-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="222fe-114">[out] Un puntero a un símbolo (token) de mensaje que se usa en el método **IMAPISession:: ShowForm** para tener acceso al mensaje que apunta _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="222fe-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="222fe-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="222fe-115">Return value</span></span>

<span data-ttu-id="222fe-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="222fe-116">S_OK</span></span> 
  
> <span data-ttu-id="222fe-117">La preparación del formulario fue correcta.</span><span class="sxs-lookup"><span data-stu-id="222fe-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="222fe-118">Notas</span><span class="sxs-lookup"><span data-stu-id="222fe-118">Remarks</span></span>

<span data-ttu-id="222fe-119">El método **IMAPISession:: PrepareForm** crea un símbolo (token) de mensaje para el mensaje que apunta el parámetro _lpMessage_ y llama a método [IUnknown:: AddRef](http://msdn.microsoft.com/es-es/library/ms691379%28v=VS.85%29.aspx) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="222fe-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](http://msdn.microsoft.com/es-es/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="222fe-120">Este token se pasa en el parámetro _ulMessageToken_ al **IMAPISession:: ShowForm**.</span><span class="sxs-lookup"><span data-stu-id="222fe-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="222fe-121">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="222fe-121">Notes to callers</span></span>

<span data-ttu-id="222fe-122">Si la llamada a **PrepareForm** se realiza correctamente, publicará el mensaje que apunta _lpMessage_ antes de llamar a **ShowForm**llamando a su método [IUnknown:: Release](http://msdn.microsoft.com/es-es/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="222fe-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](http://msdn.microsoft.com/es-es/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="222fe-123">Error al liberar el mensaje antes de llamar a **ShowForm** puede provocar pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="222fe-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="222fe-124">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="222fe-124">MFCMAPI reference</span></span>

<span data-ttu-id="222fe-125">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="222fe-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="222fe-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="222fe-126">**File**</span></span>|<span data-ttu-id="222fe-127">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="222fe-127">**Function**</span></span>|<span data-ttu-id="222fe-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="222fe-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="222fe-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="222fe-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="222fe-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="222fe-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="222fe-131">MFCMAPI usa el método **IMAPISession:: PrepareForm** , junto con **IMAPISession:: ShowForm**, para mostrar un mensaje en un formulario modal.</span><span class="sxs-lookup"><span data-stu-id="222fe-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="222fe-132">Ver también</span><span class="sxs-lookup"><span data-stu-id="222fe-132">See also</span></span>



[<span data-ttu-id="222fe-133">IMAPISession:: ShowForm</span><span class="sxs-lookup"><span data-stu-id="222fe-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="222fe-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="222fe-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="222fe-135">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="222fe-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

