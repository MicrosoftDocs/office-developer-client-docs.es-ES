---
title: IMAPISessionLogoff
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.Logoff
api_type:
- COM
ms.assetid: 93e38f6c-4b67-4f2d-bc94-631efec86852
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9dfc3b3381139b6b7fe47fb369d1cd69ee5e9677
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587841"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="5aab4-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="5aab4-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="5aab4-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5aab4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5aab4-105">Termina una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="5aab4-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="5aab4-106">Parámetros</span><span class="sxs-lookup"><span data-stu-id="5aab4-106">Parameters</span></span>

 <span data-ttu-id="5aab4-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5aab4-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="5aab4-108">[entrada] Identificador de la ventana principal de los cuadros de diálogo o windows que se mostrará.</span><span class="sxs-lookup"><span data-stu-id="5aab4-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="5aab4-109">Este parámetro se omite si no se establece la marca MAPI_LOGOFF_UI.</span><span class="sxs-lookup"><span data-stu-id="5aab4-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="5aab4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5aab4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="5aab4-111">[entrada] Una máscara de bits de indicadores que controlan la operación de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="5aab4-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="5aab4-112">Se pueden establecer los siguientes indicadores:</span><span class="sxs-lookup"><span data-stu-id="5aab4-112">The following flags can be set:</span></span>
    
<span data-ttu-id="5aab4-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="5aab4-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="5aab4-114">Si se comparte esta sesión, todos los clientes que inició la sesión mediante el uso de la sesión compartida se le deben notificar el cierre de sesión en curso.</span><span class="sxs-lookup"><span data-stu-id="5aab4-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="5aab4-115">Deben cerrar la sesión de los clientes.</span><span class="sxs-lookup"><span data-stu-id="5aab4-115">The clients should log off.</span></span> <span data-ttu-id="5aab4-116">Cualquier cliente que está usando la sesión compartida puede establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="5aab4-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="5aab4-117">MAPI_LOGOFF_SHARED se omite si no se comparte la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="5aab4-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="5aab4-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="5aab4-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="5aab4-119">**Cierre de sesión** puede mostrar un cuadro de diálogo durante la operación, posiblemente pedir confirmación al usuario.</span><span class="sxs-lookup"><span data-stu-id="5aab4-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="5aab4-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="5aab4-120">_ulReserved_</span></span>
  
> <span data-ttu-id="5aab4-121">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="5aab4-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5aab4-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="5aab4-122">Return value</span></span>

<span data-ttu-id="5aab4-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="5aab4-123">S_OK</span></span> 
  
> <span data-ttu-id="5aab4-124">La operación de cierre de sesión fue correcta.</span><span class="sxs-lookup"><span data-stu-id="5aab4-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5aab4-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="5aab4-125">Remarks</span></span>

<span data-ttu-id="5aab4-126">El método **IMAPISession::Logoff** finaliza una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="5aab4-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="5aab4-127">Cuando se devuelve el **cierre de sesión** , se puede llamar a ninguno de los métodos excepto [IUnknown:: Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="5aab4-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="5aab4-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="5aab4-128">Notes to callers</span></span>

<span data-ttu-id="5aab4-129">Cuando se devuelve el **cierre de sesión** , liberar el objeto de sesión llamando a su método **IUnknown:: Release** .</span><span class="sxs-lookup"><span data-stu-id="5aab4-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="5aab4-130">Para obtener más información acerca de terminar una sesión, vea [Finalizar una sesión de MAPI](ending-a-mapi-session.md).</span><span class="sxs-lookup"><span data-stu-id="5aab4-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5aab4-131">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5aab4-131">MFCMAPI reference</span></span>

<span data-ttu-id="5aab4-132">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="5aab4-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5aab4-133">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="5aab4-133">**File**</span></span>|<span data-ttu-id="5aab4-134">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="5aab4-134">**Function**</span></span>|<span data-ttu-id="5aab4-135">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="5aab4-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5aab4-136">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="5aab4-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="5aab4-137">CMapiObjects::Logoff</span><span class="sxs-lookup"><span data-stu-id="5aab4-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="5aab4-138">MFCMAPI usa el método **IMAPISession::Logoff** para cerrar la sesión antes de enviarlo.</span><span class="sxs-lookup"><span data-stu-id="5aab4-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="5aab4-139">Debido al comportamiento de apagado rápido que se introdujo en Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 y Microsoft Outlook 2013, los clientes nunca deben pasar el parámetro **MAPI_LOGOFF_SHARED** a [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="5aab4-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="5aab4-140">Pasando **MAPI_LOGOFF_SHARED** hará que todos los clientes MAPI empezar el cierre y se producirá un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="5aab4-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="5aab4-141">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="5aab4-141">See also</span></span>



[<span data-ttu-id="5aab4-142">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="5aab4-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="5aab4-143">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="5aab4-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="5aab4-144">Finalizar una sesión MAPI</span><span class="sxs-lookup"><span data-stu-id="5aab4-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

