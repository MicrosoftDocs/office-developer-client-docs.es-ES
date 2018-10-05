---
title: Propiedad canónica PidTagResolveMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394905"
---
# <a name="pidtagresolvemethod-canonical-property"></a>Propiedad canónica PidTagResolveMethod

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor de resolución de conflicto de la carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESOLVE_METHOD  <br/> |
|Identificador:  <br/> |0x3FE7  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad en la carpeta que contiene el mensaje de resolución de conflicto indicará cómo resolver el conflicto. Esta propiedad no es necesaria. Sin embargo, si se establece, marcas que no sea el siguiente no deben estar presentes:
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0 X 00000000)  <br/> |Conflicto resolver se debería generar el mensaje.  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0 X 00000001)  <br/> |Sobrescribir el mensaje de destino con los cambios actuales que se aplican.  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0 X 00000002)  <br/> |No enviar mensaje de notificación de conflicto al generar conflicto resolver el mensaje en la carpeta pública.  <br/> |
   
Un cliente o servidor no debe generar un mensaje de resolución de conflicto para mensajes asociados. Estos mensajes se deben resolver mediante el uso de la semántica **RESOLVE_METHOD_LAST_WRITER_WINS** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> Controla la sincronización de datos de objeto mensajería entre un servidor y un cliente.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define las estructuras de datos básicos que se usan en las operaciones remotas.
    
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

