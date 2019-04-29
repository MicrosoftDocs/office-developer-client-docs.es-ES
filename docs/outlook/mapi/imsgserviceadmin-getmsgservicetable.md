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
ms.openlocfilehash: fcaebb96d4dca4e6bfbee7491dabeafcbd93a2eb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410479"
---
# <a name="imsgserviceadmingetmsgservicetable"></a><span data-ttu-id="fcd03-103">IMsgServiceAdmin::GetMsgServiceTable</span><span class="sxs-lookup"><span data-stu-id="fcd03-103">IMsgServiceAdmin::GetMsgServiceTable</span></span>

  
  
<span data-ttu-id="fcd03-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fcd03-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fcd03-105">Proporciona acceso a la tabla servicio de mensajes, una lista de los servicios de mensajes del perfil.</span><span class="sxs-lookup"><span data-stu-id="fcd03-105">Provides access to the message service table, a list of the message services in the profile.</span></span>
  
```cpp
HRESULT GetMsgServiceTable(
  ULONG ulFlags,
  LPMAPITABLE FAR * lppTable
);
```

## <a name="parameters"></a><span data-ttu-id="fcd03-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="fcd03-106">Parameters</span></span>

 <span data-ttu-id="fcd03-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fcd03-107">_ulFlags_</span></span>
  
> <span data-ttu-id="fcd03-108">a Siempre NULL.</span><span class="sxs-lookup"><span data-stu-id="fcd03-108">[in] Always NULL.</span></span>
    
 <span data-ttu-id="fcd03-109">_lppTable_</span><span class="sxs-lookup"><span data-stu-id="fcd03-109">_lppTable_</span></span>
  
> <span data-ttu-id="fcd03-110">contempla Un puntero a un puntero a la tabla de servicio de mensajes.</span><span class="sxs-lookup"><span data-stu-id="fcd03-110">[out] A pointer to a pointer to the message service table.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fcd03-111">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="fcd03-111">Return value</span></span>

<span data-ttu-id="fcd03-112">S_OK</span><span class="sxs-lookup"><span data-stu-id="fcd03-112">S_OK</span></span> 
  
> <span data-ttu-id="fcd03-113">La tabla de servicio de mensajes se devolvió correctamente.</span><span class="sxs-lookup"><span data-stu-id="fcd03-113">The message service table was successfully returned.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fcd03-114">Comentarios</span><span class="sxs-lookup"><span data-stu-id="fcd03-114">Remarks</span></span>

<span data-ttu-id="fcd03-115">El método **IMsgServiceAdmin:: GetMsgServiceTable** proporciona acceso a la tabla de servicio de mensajes, una tabla que MAPI mantiene y enumera los servicios de mensajes instalados actualmente en el perfil de sesión.</span><span class="sxs-lookup"><span data-stu-id="fcd03-115">The **IMsgServiceAdmin::GetMsgServiceTable** method provides access to the message service table, a table that MAPI maintains that lists the message services currently installed in the session profile.</span></span> <span data-ttu-id="fcd03-116">Para obtener una lista completa de las columnas de la tabla servicio de mensajes, vea [Message Service Table](message-service-tables.md).</span><span class="sxs-lookup"><span data-stu-id="fcd03-116">For a complete list of columns in the message service table, see [Message Service Table](message-service-tables.md).</span></span>
  
<span data-ttu-id="fcd03-117">La tabla de servicio de mensajes es estática.</span><span class="sxs-lookup"><span data-stu-id="fcd03-117">The message service table is static.</span></span> <span data-ttu-id="fcd03-118">Una vez que se ha concedido acceso a un cliente, las adiciones o eliminaciones de servicios de mensajes posteriores no lo afectarán.</span><span class="sxs-lookup"><span data-stu-id="fcd03-118">After a client has been given access to it, subsequent message service additions or deletions will not affect it.</span></span> <span data-ttu-id="fcd03-119">Si no hay ningún servicio de mensajes en el perfil actual, **GetMsgServiceTable** devuelve una tabla con cero filas.</span><span class="sxs-lookup"><span data-stu-id="fcd03-119">If there are no message services in the current profile, **GetMsgServiceTable** returns a table with zero rows.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="fcd03-120">Referencia de MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="fcd03-120">MFCMAPI reference</span></span>

<span data-ttu-id="fcd03-121">Para obtener un ejemplo de código de MFCMAPI, vea la siguiente tabla.</span><span class="sxs-lookup"><span data-stu-id="fcd03-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="fcd03-122">**Archivo**</span><span class="sxs-lookup"><span data-stu-id="fcd03-122">**File**</span></span>|<span data-ttu-id="fcd03-123">**Función**</span><span class="sxs-lookup"><span data-stu-id="fcd03-123">**Function**</span></span>|<span data-ttu-id="fcd03-124">**Comentario**</span><span class="sxs-lookup"><span data-stu-id="fcd03-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="fcd03-125">MsgServiceTableDlg. cpp</span><span class="sxs-lookup"><span data-stu-id="fcd03-125">MsgServiceTableDlg.cpp</span></span>  <br/> |<span data-ttu-id="fcd03-126">CMsgServiceTableDlg:: OnRefreshView</span><span class="sxs-lookup"><span data-stu-id="fcd03-126">CMsgServiceTableDlg::OnRefreshView</span></span>  <br/> |<span data-ttu-id="fcd03-127">MFCMAPI usa el método **IMsgServiceAdmin:: GetMsgServiceTable** para cargar la tabla de servicios en un perfil para representarlo en la vista.</span><span class="sxs-lookup"><span data-stu-id="fcd03-127">MFCMAPI uses the **IMsgServiceAdmin::GetMsgServiceTable** method to load the table of services in a profile to render in the view.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fcd03-128">Ver también</span><span class="sxs-lookup"><span data-stu-id="fcd03-128">See also</span></span>



[<span data-ttu-id="fcd03-129">IMsgServiceAdmin::ConfigureMsgService</span><span class="sxs-lookup"><span data-stu-id="fcd03-129">IMsgServiceAdmin::ConfigureMsgService</span></span>](imsgserviceadmin-configuremsgservice.md)
  
[<span data-ttu-id="fcd03-130">IMsgServiceAdmin::DeleteMsgService</span><span class="sxs-lookup"><span data-stu-id="fcd03-130">IMsgServiceAdmin::DeleteMsgService</span></span>](imsgserviceadmin-deletemsgservice.md)
  
[<span data-ttu-id="fcd03-131">IMsgServiceAdmin : IUnknown</span><span class="sxs-lookup"><span data-stu-id="fcd03-131">IMsgServiceAdmin : IUnknown</span></span>](imsgserviceadminiunknown.md)


[<span data-ttu-id="fcd03-132">MFCMAPI como un ejemplo de c�digo</span><span class="sxs-lookup"><span data-stu-id="fcd03-132">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

