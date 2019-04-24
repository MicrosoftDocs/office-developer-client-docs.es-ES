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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331405"
---
# <a name="pidtagresolvemethod-canonical-property"></a>Propiedad canónica PidTagResolveMethod

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el valor de resolución de conflictos de una carpeta.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_RESOLVE_METHOD  <br/> |
|Identificador:  <br/> |0x3FE7  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Estado de MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad de la carpeta que contiene el mensaje de resolución de conflictos indicará cómo se debe resolver el conflicto. Esta propiedad no es obligatoria. Sin embargo, si se establece, las marcas que no sean las siguientes no deben estar presentes:
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0x00000000)  <br/> |Debe generarse el mensaje de resolución de conflictos.  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)  <br/> |Sobrescribir el mensaje de destino con los cambios actuales que se están aplicando.  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)  <br/> |No enviar mensaje de notificación de conflictos al generar un mensaje de conflictos de resolución en la carpeta pública.  <br/> |
   
Un cliente o un servidor no debe generar un mensaje de resolución de conflictos para los mensajes asociados. Estos mensajes deben resolverse mediante la semántica **RESOLVE_METHOD_LAST_WRITER_WINS** . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> Controla los datos de objetos de mensajería que se sincronizan entre un servidor y un cliente.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define las estructuras de datos básicas que se usan en las operaciones remotas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

