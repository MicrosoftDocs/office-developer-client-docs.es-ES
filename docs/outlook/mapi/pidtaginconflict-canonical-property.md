---
title: Propiedad canónica PidTagInConflict
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagInConflict
api_type:
- HeaderDef
ms.assetid: e83c05c6-a7c0-486c-a112-58a39255767a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fc2774efed1a15fe79e167149f2cb162bae7642c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384440"
---
# <a name="pidtaginconflict-canonical-property"></a>Propiedad canónica PidTagInConflict

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE cuando los datos adjuntos representa una réplica alternativa.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IN_CONFLICT  <br/> |
|Identificador:  <br/> |0x666C  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Nota de conflicto  <br/> |
   
## <a name="remarks"></a>Comentarios

El cliente de correo electrónico y el servidor deben generar un mensaje de resolución de conflictos cuando se detecte un conflicto con la versión actual de un mensaje en la réplica durante la sincronización. Es importante comprender que es posible que la versión actual del mensaje en la réplica local se transmite durante la operación de sincronización actual. Esto ocurrirá cuando el conflicto ya existe en el servidor antes de cualquiera de los mensajes en conflicto se han descargado a la réplica local. Un conflicto de resolver el mensaje debe sincronizarse como réplicas independientes con PCLs en conflicto. El conflicto resolver propio mensaje no debe sincronizarse entre cliente y servidor; sólo las réplicas independientes que se va a intercambiar. El asociado de sincronización, a continuación, debe generar un nuevo mensaje que coincide con la estructura del mensaje de conflicto. Por lo tanto, es importante que cliente y el servidor utilizan el mismo algoritmo para detectar el elemento "ganador". Para detectar el "ganador", se deben aplicar las siguientes reglas:
  
1. Hora de última modificación.
    
2. Superior GUID CN (mediante la comparación de memoria) para la placa de interrupción.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

