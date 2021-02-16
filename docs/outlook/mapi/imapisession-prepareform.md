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
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335771"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="58ba2-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="58ba2-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="58ba2-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="58ba2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="58ba2-105">Crea un token numérico que el [método IMAPISession::ShowForm](imapisession-showform.md) usa para tener acceso a un mensaje.</span><span class="sxs-lookup"><span data-stu-id="58ba2-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="58ba2-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="58ba2-106">Parameters</span></span>

 <span data-ttu-id="58ba2-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="58ba2-107">_lpInterface_</span></span>
  
> <span data-ttu-id="58ba2-108">[entrada] Puntero al identificador de interfaz (IID) que representa la interfaz que se usará para tener acceso al mensaje.</span><span class="sxs-lookup"><span data-stu-id="58ba2-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="58ba2-109">Pasar **los resultados** nulos en la interfaz estándar, o [IMessage](imessageimapiprop.md), que se usa.</span><span class="sxs-lookup"><span data-stu-id="58ba2-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="58ba2-110">El  _parámetro lpInterface_ debe ser **null** o IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="58ba2-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="58ba2-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="58ba2-111">_lpMessage_</span></span>
  
> <span data-ttu-id="58ba2-112">[entrada] Puntero al mensaje que se mostrará en el formulario.</span><span class="sxs-lookup"><span data-stu-id="58ba2-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="58ba2-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="58ba2-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="58ba2-114">[salida] Puntero a un token de mensaje, que usa el método **IMAPISession::ShowForm** para tener acceso al mensaje al que apunta  _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="58ba2-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="58ba2-115">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="58ba2-115">Return value</span></span>

<span data-ttu-id="58ba2-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="58ba2-116">S_OK</span></span> 
  
> <span data-ttu-id="58ba2-117">La preparación del formulario se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="58ba2-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="58ba2-118">Comentarios</span><span class="sxs-lookup"><span data-stu-id="58ba2-118">Remarks</span></span>

<span data-ttu-id="58ba2-119">El **método IMAPISession::P repareForm** crea un token de mensaje para el mensaje al que apunta el parámetro  _lpMessage_ y llama al método [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="58ba2-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="58ba2-120">Este token se pasa en el parámetro  _ulMessageToken_ a **IMAPISession::ShowForm**.</span><span class="sxs-lookup"><span data-stu-id="58ba2-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="58ba2-121">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="58ba2-121">Notes to callers</span></span>

<span data-ttu-id="58ba2-122">Si la llamada a **PrepareForm** se realiza correctamente, libere el mensaje al que apunta  _lpMessage_ llamando a su método [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) antes de llamar **a ShowForm**.</span><span class="sxs-lookup"><span data-stu-id="58ba2-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="58ba2-123">Si no se libera el mensaje antes de llamar **a ShowForm,** se pueden producir pérdidas de memoria.</span><span class="sxs-lookup"><span data-stu-id="58ba2-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="58ba2-124">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="58ba2-124">MFCMAPI reference</span></span>

<span data-ttu-id="58ba2-125">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="58ba2-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="58ba2-126">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="58ba2-126">**File**</span></span>|<span data-ttu-id="58ba2-127">**Función**</span><span class="sxs-lookup"><span data-stu-id="58ba2-127">**Function**</span></span>|<span data-ttu-id="58ba2-128">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="58ba2-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="58ba2-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="58ba2-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="58ba2-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="58ba2-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="58ba2-131">MFCMAPI usa el método **IMAPISession::P repareForm,** junto con **IMAPISession::ShowForm**, para mostrar un mensaje en un formulario modal.</span><span class="sxs-lookup"><span data-stu-id="58ba2-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="58ba2-132">Consulte también</span><span class="sxs-lookup"><span data-stu-id="58ba2-132">See also</span></span>



[<span data-ttu-id="58ba2-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="58ba2-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="58ba2-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="58ba2-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="58ba2-135">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="58ba2-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

