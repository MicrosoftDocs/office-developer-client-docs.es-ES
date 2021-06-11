---
title: Propiedad canónica PidTagStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStatus
api_type:
- COM
ms.assetid: 8b947660-eafe-47e1-9595-bd3ab7d455bf
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: de2342ef4d3e9d06f198e06dc19c65b7b144624f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278795"
---
# <a name="pidtagstatus-canonical-property"></a>Propiedad canónica PidTagStatus

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de 32 bits de marcas que definen el estado de la carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_STATUS  <br/> |
|Identificador:  <br/> |0x360B  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contenedor MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad para carpetas es análoga a **la propiedad PR_MSG_STATUS** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md)) para los mensajes. Sus marcas se proporcionan solo para la aplicación cliente y no afectan al almacén de mensajes. Los clientes pueden usar o omitir esta configuración. El cliente también puede definir sus propios valores para los bits definibles por el cliente de esta propiedad.
  
Se pueden establecer una o varias de las siguientes marcas para la máscara de bits:
  
FLDSTATUS_DELMARKED 
  
> La carpeta está marcada para su eliminación. La aplicación cliente establece esta marca.
    
FLDSTATUS_HIDDEN 
  
> La carpeta está oculta.
    
FLDSTATUS_HIGHLIGHTED 
  
> La carpeta se resalta, por ejemplo, en vídeo inverso.
    
FLDSTATUS_TAGGED 
  
> La carpeta está etiquetada.
    
Los proveedores de almacén de mensajes establecen esta propiedad en una carpeta en uno o varios de estos valores y los clientes interpretan el estado según corresponda para sus aplicaciones. Por ejemplo, un cliente puede usar el estado de la carpeta para diferenciar visualmente entre carpetas de una tabla de jerarquía, mostrando carpetas con el mismo estado de la misma manera. Las carpetas resaltadas se pueden mostrar en vídeo inverso, las carpetas etiquetadas y las carpetas marcadas para su eliminación se pueden mostrar con un icono significativo y las carpetas ocultas se pueden ocultar.
  
Los bits del 16 al 31 ("0x10000" a "0x80000000") de esta propiedad están disponibles para su uso en la aplicación cliente de IPM. Todos los demás bits están reservados para su uso por MAPI; los que no están definidos en la lista anterior deben establecerse inicialmente en cero y no modificarse.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

