---
title: ITableDataHrNotify
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITableData.HrNotify
api_type:
- COM
ms.assetid: 98548b50-342e-434a-9ad3-c37ba418c5ce
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 1be4fd95d29859c542fe553bdc3728ea23444694
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817988"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="52dcf-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="52dcf-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="52dcf-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="52dcf-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="52dcf-105">Envía una notificación para una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="52dcf-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="52dcf-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="52dcf-106">Parameters</span></span>

 <span data-ttu-id="52dcf-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="52dcf-107">_ulFlags_</span></span>
  
> <span data-ttu-id="52dcf-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="52dcf-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="52dcf-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="52dcf-109">_cValues_</span></span>
  
> <span data-ttu-id="52dcf-110">[entrada] El recuento de valores de propiedad en la estructura [SPropValue](spropvalue.md) indicada por el parámetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="52dcf-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="52dcf-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="52dcf-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="52dcf-112">[entrada] Un puntero a una estructura **SPropValue** que se describe los valores de las columnas de la fila de destino.</span><span class="sxs-lookup"><span data-stu-id="52dcf-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="52dcf-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="52dcf-113">Return value</span></span>

<span data-ttu-id="52dcf-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="52dcf-114">S_OK</span></span> 
  
> <span data-ttu-id="52dcf-115">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="52dcf-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="52dcf-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="52dcf-116">Remarks</span></span>

<span data-ttu-id="52dcf-117">El método **ITableData::HrNotify** envía una notificación de TABLE_ROW_MODIFIED para la fila que coincide con la fila que se describen las propiedades que apunta el parámetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="52dcf-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="52dcf-118">**HrNotify** envía la notificación, independientemente de si se han producido cambios en la fila.</span><span class="sxs-lookup"><span data-stu-id="52dcf-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="52dcf-119">Todos los clientes y proveedores de servicios que tienen las vistas de la tabla y han llamado [IMAPITable::Advise](imapitable-advise.md) para registrar las notificaciones en las vistas de reciben esta notificación.</span><span class="sxs-lookup"><span data-stu-id="52dcf-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52dcf-120">Vea también</span><span class="sxs-lookup"><span data-stu-id="52dcf-120">See also</span></span>



[<span data-ttu-id="52dcf-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="52dcf-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="52dcf-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="52dcf-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="52dcf-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52dcf-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)
