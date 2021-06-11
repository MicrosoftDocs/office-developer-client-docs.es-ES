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
ms.openlocfilehash: 317c3702415ddf30038ccd0d40cdf0f19abc61f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338111"
---
# <a name="imapisessionlogoff"></a><span data-ttu-id="1374c-103">IMAPISession::Logoff</span><span class="sxs-lookup"><span data-stu-id="1374c-103">IMAPISession::Logoff</span></span>

  
  
<span data-ttu-id="1374c-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1374c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1374c-105">Finaliza una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="1374c-105">Ends a MAPI session.</span></span>
  
```cpp
HRESULT Logoff(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  ULONG ulReserved
);
```

## <a name="parameters"></a><span data-ttu-id="1374c-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="1374c-106">Parameters</span></span>

 <span data-ttu-id="1374c-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1374c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1374c-108">[in] Identificador de la ventana principal de los cuadros de diálogo o ventanas que se mostrarán.</span><span class="sxs-lookup"><span data-stu-id="1374c-108">[in] A handle to the parent window of any dialog boxes or windows to be displayed.</span></span> <span data-ttu-id="1374c-109">Este parámetro se omite si no se MAPI_LOGOFF_UI marca.</span><span class="sxs-lookup"><span data-stu-id="1374c-109">This parameter is ignored if the MAPI_LOGOFF_UI flag is not set.</span></span>
    
 <span data-ttu-id="1374c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1374c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="1374c-111">[in] Máscara de bits de marcas que controlan la operación de cierre de sesión.</span><span class="sxs-lookup"><span data-stu-id="1374c-111">[in] A bitmask of flags that control the logoff operation.</span></span> <span data-ttu-id="1374c-112">Se pueden establecer las siguientes marcas:</span><span class="sxs-lookup"><span data-stu-id="1374c-112">The following flags can be set:</span></span>
    
<span data-ttu-id="1374c-113">MAPI_LOGOFF_SHARED</span><span class="sxs-lookup"><span data-stu-id="1374c-113">MAPI_LOGOFF_SHARED</span></span> 
  
> <span data-ttu-id="1374c-114">Si se comparte esta sesión, todos los clientes que iniciaron sesión con la sesión compartida deben recibir una notificación del cierre de sesión en curso.</span><span class="sxs-lookup"><span data-stu-id="1374c-114">If this session is shared, all clients that logged on by using the shared session should be notified of the logoff in progress.</span></span> <span data-ttu-id="1374c-115">Los clientes deben cerrar sesión.</span><span class="sxs-lookup"><span data-stu-id="1374c-115">The clients should log off.</span></span> <span data-ttu-id="1374c-116">Cualquier cliente que use la sesión compartida puede establecer esta marca.</span><span class="sxs-lookup"><span data-stu-id="1374c-116">Any client that is using the shared session can set this flag.</span></span> <span data-ttu-id="1374c-117">MAPI_LOGOFF_SHARED se omite si no se comparte la sesión actual.</span><span class="sxs-lookup"><span data-stu-id="1374c-117">MAPI_LOGOFF_SHARED is ignored if the current session is not shared.</span></span>
    
<span data-ttu-id="1374c-118">MAPI_LOGOFF_UI</span><span class="sxs-lookup"><span data-stu-id="1374c-118">MAPI_LOGOFF_UI</span></span> 
  
> <span data-ttu-id="1374c-119">**La cierre de** sesión puede mostrar un cuadro de diálogo durante la operación, lo que puede pedir confirmación al usuario.</span><span class="sxs-lookup"><span data-stu-id="1374c-119">**Logoff** can display a dialog box during the operation, possibly prompting the user for confirmation.</span></span> 
    
 <span data-ttu-id="1374c-120">_ulReserved_</span><span class="sxs-lookup"><span data-stu-id="1374c-120">_ulReserved_</span></span>
  
> <span data-ttu-id="1374c-121">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="1374c-121">[in] Reserved; must be zero.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1374c-122">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="1374c-122">Return value</span></span>

<span data-ttu-id="1374c-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="1374c-123">S_OK</span></span> 
  
> <span data-ttu-id="1374c-124">La operación de cierre de sesión se ha realizado correctamente.</span><span class="sxs-lookup"><span data-stu-id="1374c-124">The logoff operation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1374c-125">Comentarios</span><span class="sxs-lookup"><span data-stu-id="1374c-125">Remarks</span></span>

<span data-ttu-id="1374c-126">El **método IMAPISession::Logoff** finaliza una sesión MAPI.</span><span class="sxs-lookup"><span data-stu-id="1374c-126">The **IMAPISession::Logoff** method ends a MAPI session.</span></span> <span data-ttu-id="1374c-127">Cuando **logoff** devuelve, no se puede llamar a ninguno de los métodos excepto [IUnknown::Release.](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="1374c-127">When **Logoff** returns, none of the methods except for [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) can be called.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1374c-128">Notas para los llamadores</span><span class="sxs-lookup"><span data-stu-id="1374c-128">Notes to callers</span></span>

<span data-ttu-id="1374c-129">Cuando **logoff** devuelve, libera el objeto de sesión llamando a su **método IUnknown::Release.**</span><span class="sxs-lookup"><span data-stu-id="1374c-129">When **Logoff** returns, release the session object by calling its **IUnknown::Release** method.</span></span> 
  
<span data-ttu-id="1374c-130">Para obtener más información acerca de cómo finalizar una sesión, vea [Ending a MAPI Session](ending-a-mapi-session.md).</span><span class="sxs-lookup"><span data-stu-id="1374c-130">For more information about ending a session, see [Ending a MAPI Session](ending-a-mapi-session.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1374c-131">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1374c-131">MFCMAPI reference</span></span>

<span data-ttu-id="1374c-132">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="1374c-132">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1374c-133">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="1374c-133">**File**</span></span>|<span data-ttu-id="1374c-134">**Función**</span><span class="sxs-lookup"><span data-stu-id="1374c-134">**Function**</span></span>|<span data-ttu-id="1374c-135">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="1374c-135">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1374c-136">MAPIObjects.cpp</span><span class="sxs-lookup"><span data-stu-id="1374c-136">MAPIObjects.cpp</span></span>  <br/> |<span data-ttu-id="1374c-137">CMapiObjects::Logoff</span><span class="sxs-lookup"><span data-stu-id="1374c-137">CMapiObjects::Logoff</span></span>  <br/> |<span data-ttu-id="1374c-138">MFCMAPI usa el **método IMAPISession::Logoff** para cerrar sesión de la sesión antes de liberarla.</span><span class="sxs-lookup"><span data-stu-id="1374c-138">MFCMAPI uses the **IMAPISession::Logoff** method to log off from the session before releasing it.</span></span>  <br/> |
   
> [!NOTE]
> <span data-ttu-id="1374c-139">Debido al comportamiento de apagado rápido introducido en Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010 y Microsoft Outlook 2013, los clientes nunca deben pasar el parámetro **MAPI_LOGOFF_SHARED a** [IMAPISession::Logoff](imapisession-logoff.md).</span><span class="sxs-lookup"><span data-stu-id="1374c-139">Due to the fast shutdown behavior introduced in Microsoft Office Outlook 2007 Service Pack 2, Microsoft Outlook 2010, and Microsoft Outlook 2013, clients should never pass the **MAPI_LOGOFF_SHARED** parameter to [IMAPISession::Logoff](imapisession-logoff.md).</span></span> <span data-ttu-id="1374c-140">Pasar **MAPI_LOGOFF_SHARED** hará que todos los clientes MAPI comiencen a cerrarse y se producirá un comportamiento inesperado.</span><span class="sxs-lookup"><span data-stu-id="1374c-140">Passing **MAPI_LOGOFF_SHARED** will cause all MAPI clients to begin shutdown and unexpected behavior will occur.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1374c-141">Vea también</span><span class="sxs-lookup"><span data-stu-id="1374c-141">See also</span></span>



[<span data-ttu-id="1374c-142">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1374c-142">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="1374c-143">MFCMAPI como un ejemplo de código</span><span class="sxs-lookup"><span data-stu-id="1374c-143">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="1374c-144">Finalización de una sesión MAPI</span><span class="sxs-lookup"><span data-stu-id="1374c-144">Ending a MAPI Session</span></span>](ending-a-mapi-session.md)

