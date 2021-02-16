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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358537"
---
# <a name="pidtaginconflict-canonical-property"></a>Propiedad canónica PidTagInConflict

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene TRUE cuando los datos adjuntos representan una réplica alternativa.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IN_CONFLICT  <br/> |
|Identificador:  <br/> |0x666C  <br/> |
|Tipo de datos:  <br/> |PT_BOOLEAN  <br/> |
|Área:  <br/> |Nota de conflicto  <br/> |
   
## <a name="remarks"></a>Comentarios

El cliente de correo electrónico y el servidor deben generar un mensaje de resolución de conflictos al detectar un conflicto con la versión actual de un mensaje en la réplica durante la sincronización. Es importante comprender que es posible que la versión actual del mensaje en la réplica local se transmita durante la operación de sincronización actual. Esto ocurrirá cuando el conflicto ya exista en el servidor antes de que cualquiera de los mensajes en conflicto se descargara en la réplica local. Un mensaje de resolución de conflictos debe sincronizarse como réplicas independientes con PCL en conflicto. El mensaje de resolución de conflictos no debe sincronizarse entre el cliente y el servidor; solo se deben intercambiar las réplicas independientes. A continuación, el asociado de sincronización debe generar un nuevo mensaje que coincida con la estructura del mensaje en conflicto. Por lo tanto, es importante que el cliente y el servidor usen el mismo algoritmo para detectar el elemento "ganador". Se deben aplicar las siguientes reglas para detectar el "ganador":
  
1. Hora de la última modificación.
    
2. GUID de CN más alto (con comparación de memoria) para romper la vinculación.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Controla la sincronización de datos de objetos de mensajería entre un servidor y un cliente.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

