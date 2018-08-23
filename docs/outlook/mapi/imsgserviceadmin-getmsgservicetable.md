---
title: IMsgServiceAdminGetMsgServiceTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgServiceAdmin.GetMsgServiceTable
api_type:
- COM
ms.assetid: 064dd5ca-0108-4045-b17b-0bb29cb93346
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 5d8e91490cc39c3f259d35a923bb3bcbb2bf6011
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568171"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="8da76-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="8da76-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="8da76-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8da76-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8da76-105">Proporciona acceso a la tabla de servicio de mensajes, una lista de los servicios de mensaje en el perfil.</span><span class="sxs-lookup"><span data-stu-id="8da76-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="8da76-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="8da76-106">Parameters</span></span>

 <span data-ttu-id="8da76-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="8da76-107">_ulFlags_</span></span>
  
> <span data-ttu-id="8da76-108">[entrada] Siempre es NULL.</span><span class="sxs-lookup"><span data-stu-id="8da76-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="8da76-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="8da76-109">_lppTable_</span></span>
  
> <span data-ttu-id="8da76-110">[out] Un puntero a un puntero a la tabla de mensajes de servicio.</span><span class="sxs-lookup"><span data-stu-id="8da76-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8da76-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="8da76-111">Return value</span></span>

<span data-ttu-id="8da76-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="8da76-112">S_OK</span></span> 
  
> <span data-ttu-id="8da76-113">La tabla de mensajes de servicio se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="8da76-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8da76-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="8da76-114">Remarks</span></span>

<span data-ttu-id="8da76-115">El método **IMsgServiceAdmin::GetMsgServiceTable** proporciona acceso a la tabla de servicio de mensajes, una tabla que mantiene MAPI que se enumera los servicios de mensaje instalados actualmente en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="8da76-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="8da76-116">Para obtener una lista completa de las columnas en la tabla de servicios de mensaje, vea [Tabla de mensajes de servicio](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="8da76-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="8da76-117">En la tabla de servicio del mensaje es estática.</span><span class="sxs-lookup"><span data-stu-id="8da76-117">The message service table is static.</span></span> <span data-ttu-id="8da76-118">Después de que un cliente se han concedido acceso a él, mensaje subsiguientes servicio incorporaciones o eliminaciones no afectará a él.</span><span class="sxs-lookup"><span data-stu-id="8da76-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="8da76-119">Si no hay ningún servicio de mensaje en el perfil actual, **GetMsgServiceTable** devuelve un objeto table con cero filas.</span><span class="sxs-lookup"><span data-stu-id="8da76-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8da76-120">Referencia MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="8da76-120">MFCMAPI reference</span></span>

<span data-ttu-id="8da76-121">MFCMAPI c�digo de ejemplo, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="8da76-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8da76-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="8da76-122">**File**</span></span>|<span data-ttu-id="8da76-123">**Funci�n**</span><span class="sxs-lookup"><span data-stu-id="8da76-123">**Function**</span></span>|<span data-ttu-id="8da76-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="8da76-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8da76-125">MsgServiceTableDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="8da76-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="8da76-126">CMsgServiceTableDlg::OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="8da76-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="8da76-127">MFCMAPI utiliza el método **IMsgServiceAdmin::GetMsgServiceTable** para cargar en la tabla de servicios en un perfil para representar en la vista.</span><span class="sxs-lookup"><span data-stu-id="8da76-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8da76-128">Recursos adicionales</span><span class="sxs-lookup"><span data-stu-id="8da76-128">See also</span></span>



[<span data-ttu-id="8da76-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="8da76-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="8da76-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="8da76-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="8da76-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8da76-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="8da76-132">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="8da76-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

