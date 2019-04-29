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
ms.openlocfilehash: aa2170bf4bedfb441ad4808f774f6f71d5caf85e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33413272"
---
# <a name="itabledatahrnotify"></a><span data-ttu-id="719fd-103">ITableData::HrNotify</span><span class="sxs-lookup"><span data-stu-id="719fd-103">ITableData::HrNotify</span></span>

  
  
<span data-ttu-id="719fd-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="719fd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="719fd-105">Envía una notificación para una fila de tabla.</span><span class="sxs-lookup"><span data-stu-id="719fd-105">Sends a notification for a table row.</span></span>
  
```cpp
HRESULT HrNotify(
  ULONG ulFlags,
  ULONG cValues,
  LPSPropValue lpSPropValue
);
```

## <a name="parameters"></a><span data-ttu-id="719fd-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="719fd-106">Parameters</span></span>

 <span data-ttu-id="719fd-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="719fd-107">_ulFlags_</span></span>
  
> <span data-ttu-id="719fd-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="719fd-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="719fd-109">_cValues_</span><span class="sxs-lookup"><span data-stu-id="719fd-109">_cValues_</span></span>
  
> <span data-ttu-id="719fd-110">a El número de valores de propiedad en la estructura [SPropValue](spropvalue.md) apuntado por el parámetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="719fd-110">[in] The count of property values in the [SPropValue](spropvalue.md) structure pointed to by the  _lpSPropValue_ parameter.</span></span> 
    
 <span data-ttu-id="719fd-111">_lpSPropValue_</span><span class="sxs-lookup"><span data-stu-id="719fd-111">_lpSPropValue_</span></span>
  
> <span data-ttu-id="719fd-112">a Un puntero a una estructura **SPropValue** que describe los valores de las columnas en la fila de destino.</span><span class="sxs-lookup"><span data-stu-id="719fd-112">[in] A pointer to an **SPropValue** structure that describes the values of the columns in the target row.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="719fd-113">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="719fd-113">Return value</span></span>

<span data-ttu-id="719fd-114">S_OK</span><span class="sxs-lookup"><span data-stu-id="719fd-114">S_OK</span></span> 
  
> <span data-ttu-id="719fd-115">La llamada se ha realizado correctamente y devuelva el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="719fd-115">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="719fd-116">Comentarios</span><span class="sxs-lookup"><span data-stu-id="719fd-116">Remarks</span></span>

<span data-ttu-id="719fd-117">El método **ITableData:: HrNotify** envía una notificación de TABLE_ROW_MODIFIED para la fila que coincide con la fila descrita por las propiedades a las que apunta el parámetro _lpSPropValue_ .</span><span class="sxs-lookup"><span data-stu-id="719fd-117">The **ITableData::HrNotify** method sends a TABLE_ROW_MODIFIED notification for the row that matches the row described by the properties pointed to by the  _lpSPropValue_ parameter.</span></span> <span data-ttu-id="719fd-118">**HrNotify** envía la notificación independientemente de si se han producido cambios en la fila.</span><span class="sxs-lookup"><span data-stu-id="719fd-118">**HrNotify** sends the notification regardless of whether changes have occurred to the row.</span></span> <span data-ttu-id="719fd-119">Todos los clientes y proveedores de servicios que tienen vistas de la tabla y han llamado a [IMAPITable:: Advise](imapitable-advise.md) para registrarse en las notificaciones en sus vistas reciben esta notificación.</span><span class="sxs-lookup"><span data-stu-id="719fd-119">All clients and service providers that have views of the table and have called [IMAPITable::Advise](imapitable-advise.md) to register for notifications on their views receive this notification.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="719fd-120">Ver también</span><span class="sxs-lookup"><span data-stu-id="719fd-120">See also</span></span>



[<span data-ttu-id="719fd-121">SPropValue</span><span class="sxs-lookup"><span data-stu-id="719fd-121">SPropValue</span></span>](spropvalue.md)
  
[<span data-ttu-id="719fd-122">TABLE_NOTIFICATION</span><span class="sxs-lookup"><span data-stu-id="719fd-122">TABLE_NOTIFICATION</span></span>](table_notification.md)
  
[<span data-ttu-id="719fd-123">ITableData : IUnknown</span><span class="sxs-lookup"><span data-stu-id="719fd-123">ITableData : IUnknown</span></span>](itabledataiunknown.md)

