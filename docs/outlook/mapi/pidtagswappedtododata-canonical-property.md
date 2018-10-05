---
title: Propiedad canónica PidTagSwappedToDoData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSwappedToDoData
api_type:
- COM
ms.assetid: d2a82fc8-de5d-4819-906e-b8314fd06ea0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 3ecfa1e89688ae525a28e221424fb4a8194fc217
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25386673"
---
# <a name="pidtagswappedtododata-canonical-property"></a>Propiedad canónica PidTagSwappedToDoData

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Mantiene un segundo conjunto de valores de propiedad que no influyen en el estado del objeto de mensaje marcado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SWAPPED_TODO_DATA  <br/> |
|Identificador:  <br/> |0x0E2D  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |MAPI no transmisible  <br/> |
   
## <a name="remarks"></a>Comentarios

Actúa como la ubicación de almacenamiento marca secundaria si son compatibles con marcas de remitente o avisos de remitente, esta estructura proporciona una ubicación en la que se va a almacenar todas las propiedades relacionadas con el protocolo de marcar informativos que son compatibles con marcas de remitente y todas propiedades relacionadas con el protocolo de configuración de aviso que son compatibles con los avisos de remitente sin exponer la información de aviso de remitente a los destinatarios de un mensaje o un indicador de remitente.
  
De forma similar, esta estructura proporciona una ubicación en la que se va a almacenar todas las propiedades relacionadas con el protocolo de marcar informativos que son compatibles con marcas de destinatarios y propiedades relacionadas con el protocolo de configuración de aviso que son compatibles con destinatario avisos en un mensaje enviado anteriormente.
  
Para obtener más información acerca de esta propiedad, vea [[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones relacionadas con marcas.
    
[[MS-OXORMDR]](https://msdn.microsoft.com/library/5454ebcc-e5d1-4da8-a598-d393b101caab%28Office.15%29.aspx)
  
> Especifica las propiedades y el modelo de interacción para correo electrónico y otros avisos de objeto.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

