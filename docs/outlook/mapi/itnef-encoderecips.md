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
ms.openlocfilehash: edabb9a0f55cb34b4e144672e91ea50b8e9193b0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19817982"
---
# <a name="itnefencoderecips"></a><span data-ttu-id="48484-103">ITnef::EncodeRecips</span><span class="sxs-lookup"><span data-stu-id="48484-103">ITnef::EncodeRecips</span></span>

  
  
<span data-ttu-id="48484-104">**Hace referencia a**: Outlook</span><span class="sxs-lookup"><span data-stu-id="48484-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="48484-105">Codifica una vista de tabla de destinatarios de un mensaje en la secuencia de datos de formato de encapsulación neutro para el transporte (TNEF) para el mensaje.</span><span class="sxs-lookup"><span data-stu-id="48484-105">Encodes a view for a message's recipient table in the Transport-Neutral Encapsulation Format (TNEF) data stream for the message.</span></span>
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a><span data-ttu-id="48484-106">Par�metros</span><span class="sxs-lookup"><span data-stu-id="48484-106">Parameters</span></span>

 <span data-ttu-id="48484-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="48484-107">_ulFlags_</span></span>
  
> <span data-ttu-id="48484-108">[entrada] Reservado; debe ser cero.</span><span class="sxs-lookup"><span data-stu-id="48484-108">[in] Reserved; must be zero.</span></span>
    
 <span data-ttu-id="48484-109">_lpRecipientTable_</span><span class="sxs-lookup"><span data-stu-id="48484-109">_lpRecipientTable_</span></span>
  
> <span data-ttu-id="48484-110">[entrada] Un puntero a la tabla de destinatarios para el que se codifica la vista.</span><span class="sxs-lookup"><span data-stu-id="48484-110">[in] A pointer to the recipient table for which the view is encoded.</span></span> <span data-ttu-id="48484-111">El parámetro _lpRecipientTable_ puede ser NULL.</span><span class="sxs-lookup"><span data-stu-id="48484-111">The  _lpRecipientTable_ parameter can be NULL.</span></span> 
    
## <a name="return-value"></a><span data-ttu-id="48484-112">Valor devuelto</span><span class="sxs-lookup"><span data-stu-id="48484-112">Return value</span></span>

<span data-ttu-id="48484-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="48484-113">S_OK</span></span> 
  
> <span data-ttu-id="48484-114">La llamada se ha realizado correctamente y devuelve el valor esperado o los valores.</span><span class="sxs-lookup"><span data-stu-id="48484-114">The call succeeded and returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="48484-115">Comentarios</span><span class="sxs-lookup"><span data-stu-id="48484-115">Remarks</span></span>

<span data-ttu-id="48484-116">Transporte proveedores, los proveedores de almacén de mensajes y las puertas de enlace llamada al método **ITnef::EncodeRecips** para llevar a cabo la codificación TNEF para una vista de tabla de destinatarios determinada.</span><span class="sxs-lookup"><span data-stu-id="48484-116">Transport providers, message store providers, and gateways call the **ITnef::EncodeRecips** method to perform TNEF encoding for a particular recipient table view.</span></span> <span data-ttu-id="48484-117">La codificación TNEF es útil, por ejemplo, si un proveedor o una puerta de enlace requiere un conjunto de columnas determinado, criterio de ordenación o restricción para la tabla de destinatarios.</span><span class="sxs-lookup"><span data-stu-id="48484-117">TNEF encoding is useful, for example, if a provider or gateway requires a particular column set, sort order, or restriction for the recipient table.</span></span> 
  
<span data-ttu-id="48484-118">Un proveedor o una puerta de enlace pasa la vista de tabla que se desea codificar en el parámetro _lpRecipientTable_ .</span><span class="sxs-lookup"><span data-stu-id="48484-118">A provider or gateway passes the table view to be encoded in the  _lpRecipientTable_ parameter.</span></span> <span data-ttu-id="48484-119">La implementación de TNEF codifica la tabla de destinatarios con la vista determinada, con el conjunto de columnas determinado, criterio de ordenación, restricción y posición.</span><span class="sxs-lookup"><span data-stu-id="48484-119">The TNEF implementation encodes the recipient table with the given view, using the given column set, sort order, restriction, and position.</span></span> <span data-ttu-id="48484-120">Si un proveedor o una puerta de enlace pasa NULL en _lpRecipientTable_, TNEF Obtiene la tabla de destinatarios del mensaje se codifica mediante el método [IMessage::GetRecipientTable](imessage-getrecipienttable.md) y procesa cada fila de la tabla en la secuencia de TNEF mediante la configuración actual de la tabla.</span><span class="sxs-lookup"><span data-stu-id="48484-120">If a provider or gateway passes NULL in  _lpRecipientTable_, TNEF gets the recipient table from the message being encoded by using the [IMessage::GetRecipientTable](imessage-getrecipienttable.md) method, and processes every row of the table into the TNEF stream by using the table's current settings.</span></span> 
  
<span data-ttu-id="48484-121">Por tanto, al llamar a **EncodeRecips** con NULL _lpRecipientTable_ codifica a todos los destinatarios del mensaje y es equivalente a llamar al método [ITnef::AddProps](itnef-addprops.md) con la marca TNEF_PROP_INCLUDE en su parámetro _ulFlags_ y la **PR_ MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) (propiedad) en su parámetro _lpPropList_ .</span><span class="sxs-lookup"><span data-stu-id="48484-121">Calling **EncodeRecips** with NULL in  _lpRecipientTable_ thus encodes all message recipients and is equivalent to calling the [ITnef::AddProps](itnef-addprops.md) method with the TNEF_PROP_INCLUDE flag in its  _ulFlags_ parameter and the **PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) property in its  _lpPropList_ parameter.</span></span> 
  
<span data-ttu-id="48484-122">Tenga en cuenta que es rara vez es necesario llamar a **EncodeRecips** a menos que haya un requisito para codificar una vista de tabla de destinatarios determinada.</span><span class="sxs-lookup"><span data-stu-id="48484-122">Note that it is rarely necessary to call **EncodeRecips** unless there is a requirement to encode a particular recipient table view.</span></span> <span data-ttu-id="48484-123">Sistemas de mensajería externos casi siempre tengan instalaciones para el tratamiento de las listas de destinatarios que son lo suficientemente eficaces para controlar las necesidades comunes de codificación de las listas de destinatarios; por lo tanto, estos sistemas casi nunca requieran la codificación TNEF para este propósito.</span><span class="sxs-lookup"><span data-stu-id="48484-123">Foreign messaging systems almost always have facilities for handling recipient lists that are powerful enough to handle the common needs of encoding recipient lists; therefore, these systems almost never require TNEF for this purpose.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="48484-124">Vea también</span><span class="sxs-lookup"><span data-stu-id="48484-124">See also</span></span>



[<span data-ttu-id="48484-125">IMessage::GetRecipientTable</span><span class="sxs-lookup"><span data-stu-id="48484-125">IMessage::GetRecipientTable</span></span>](imessage-getrecipienttable.md)
  
[<span data-ttu-id="48484-126">ITnef::AddProps</span><span class="sxs-lookup"><span data-stu-id="48484-126">ITnef::AddProps</span></span>](itnef-addprops.md)
  
[<span data-ttu-id="48484-127">Propiedad canónica PidTagMessageRecipients</span><span class="sxs-lookup"><span data-stu-id="48484-127">PidTagMessageRecipients Canonical Property</span></span>](pidtagmessagerecipients-canonical-property.md)
  
[<span data-ttu-id="48484-128">ITnef : IUnknown</span><span class="sxs-lookup"><span data-stu-id="48484-128">ITnef : IUnknown</span></span>](itnefiunknown.md)

