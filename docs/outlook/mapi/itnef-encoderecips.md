---
title: ITnefEncodeRecips
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ITnef.EncodeRecips
api_type:
- COM
ms.assetid: b3ce4b0e-4f48-4a7e-a30c-c4754bccb12c
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: d8caa503e557d35e259db743505d39ea4809dbfd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348660"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="d2e9f-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="d2e9f-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="d2e9f-104">**Se aplica a**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d2e9f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d2e9f-105">Codifica una vista para la tabla de destinatarios de un mensaje en el flujo de datos TNEF (formato de encapsulación neutro para el transporte) del mensaje.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="d2e9f-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d2e9f-106">Parameters</span></span>

 <span data-ttu-id="d2e9f-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d2e9f-107">_ulFlags_</span></span>
  
> <span data-ttu-id="d2e9f-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="d2e9f-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="d2e9f-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="d2e9f-110">a Un puntero a la tabla de destinatarios para la que está codificada la vista.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="d2e9f-111">El parámetro _lpRecipientTable_ puede ser null.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="d2e9f-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="d2e9f-112">Return value</span></span>

<span data-ttu-id="d2e9f-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="d2e9f-113">S_OK</span></span> 
  
> <span data-ttu-id="d2e9f-114">La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d2e9f-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="d2e9f-115">Remarks</span></span>

<span data-ttu-id="d2e9f-116">Los proveedores de transporte, los proveedores de almacenamiento de mensajes y las puertas de enlace llaman al método **ITnef:: EncodeRecips** para realizar la codificación TNEF para una vista de tabla de destinatarios determinada.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="d2e9f-117">La codificación TNEF es útil, por ejemplo, si un proveedor o una puerta de enlace requiere un conjunto de columnas, un criterio de ordenación o una restricción concretos para la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="d2e9f-118">Un proveedor o una puerta de enlace pasa la vista de tabla que se va a codificar en el parámetro _lpRecipientTable_ .</span><span class="sxs-lookup"><span data-stu-id="d2e9f-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="d2e9f-119">La implementación de TNEF codifica la tabla de destinatarios con la vista determinada, usando el conjunto de columnas, el criterio de ordenación, la restricción y la posición dados.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="d2e9f-120">Si un proveedor o una puerta de enlace pasa NULL en _lpRecipientTable_, TNEF obtiene la tabla de destinatarios del mensaje que se está codificando mediante el método [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) y procesa todas las filas de la tabla en la secuencia TNEF mediante el configuración actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="d2e9f-121">Al llamar a **EncodeRecips** con NULL en _lpRecipientTable_ , se codifican todos los destinatarios del mensaje y equivale a llamar al método [ITnef:: AddProps](itnef-addprops.md) con la marca TNEF_PROP_INCLUDE en su parámetro _ulFlags_ y el **PR_ Propiedad MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en su parámetro _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="d2e9f-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="d2e9f-122">Tenga en cuenta que rara vez es necesario llamar a **EncodeRecips** a menos que haya un requisito para codificar una vista de tabla de destinatarios determinada.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="d2e9f-123">Los sistemas de mensajería externos casi siempre tienen instalaciones para administrar listas de destinatarios que son lo suficientemente eficaces como para controlar las necesidades comunes de codificación de listas de destinatarios; por lo tanto, estos sistemas casi nunca requieren TNEF para este propósito.</span><span class="sxs-lookup"><span data-stu-id="d2e9f-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d2e9f-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="d2e9f-124">See also</span></span>



[<span data-ttu-id="d2e9f-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="d2e9f-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="d2e9f-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="d2e9f-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="d2e9f-127">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="d2e9f-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="d2e9f-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d2e9f-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

