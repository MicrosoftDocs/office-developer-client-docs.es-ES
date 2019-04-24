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
# <a name="itnefencoderecips"></a>ITnef::EncodeRecips

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Codifica una vista para la tabla de destinatarios de un mensaje en el flujo de datos TNEF (formato de encapsulación neutro para el transporte) del mensaje.
  
```cpp
HRESULT EncodeRecips(
  ULONG ulFlags,
  LPMAPITABLE lpRecipientTable
);
```

## <a name="parameters"></a>Parameters

 _ulFlags_
  
> [entrada] Reservado; debe ser cero.
    
 _lpRecipientTable_
  
> a Un puntero a la tabla de destinatarios para la que está codificada la vista. El parámetro _lpRecipientTable_ puede ser null. 
    
## <a name="return-value"></a>Valor devuelto

S_OK 
  
> La llamada se ha realizado correctamente y ha devuelto el valor o los valores esperados.
    
## <a name="remarks"></a>Comentarios

Los proveedores de transporte, los proveedores de almacenamiento de mensajes y las puertas de enlace llaman al método **ITnef:: EncodeRecips** para realizar la codificación TNEF para una vista de tabla de destinatarios determinada. La codificación TNEF es útil, por ejemplo, si un proveedor o una puerta de enlace requiere un conjunto de columnas, un criterio de ordenación o una restricción concretos para la tabla de destinatarios. 
  
Un proveedor o una puerta de enlace pasa la vista de tabla que se va a codificar en el parámetro _lpRecipientTable_ . La implementación de TNEF codifica la tabla de destinatarios con la vista determinada, usando el conjunto de columnas, el criterio de ordenación, la restricción y la posición dados. Si un proveedor o una puerta de enlace pasa NULL en _lpRecipientTable_, TNEF obtiene la tabla de destinatarios del mensaje que se está codificando mediante el método [IMessage:: GetRecipientTable](imessage-getrecipienttable.md) y procesa todas las filas de la tabla en la secuencia TNEF mediante el configuración actual de la tabla. 
  
Al llamar a **EncodeRecips** con NULL en _lpRecipientTable_ , se codifican todos los destinatarios del mensaje y equivale a llamar al método [ITnef:: AddProps](itnef-addprops.md) con la marca TNEF_PROP_INCLUDE en su parámetro _ulFlags_ y el **PR_ Propiedad MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)) en su parámetro _lpPropList_ . 
  
Tenga en cuenta que rara vez es necesario llamar a **EncodeRecips** a menos que haya un requisito para codificar una vista de tabla de destinatarios determinada. Los sistemas de mensajería externos casi siempre tienen instalaciones para administrar listas de destinatarios que son lo suficientemente eficaces como para controlar las necesidades comunes de codificación de listas de destinatarios; por lo tanto, estos sistemas casi nunca requieren TNEF para este propósito. 
  
## <a name="see-also"></a>Vea también



[IMessage::GetRecipientTable](imessage-getrecipienttable.md)
  
[ITnef::AddProps](itnef-addprops.md)
  
[Propiedad canónica PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md)
  
[ITnef : IUnknown](itnefiunknown.md)

