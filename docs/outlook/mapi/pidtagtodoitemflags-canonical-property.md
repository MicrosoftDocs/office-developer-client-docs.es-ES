---
title: Propiedad canónica PidTagToDoItemFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagToDoItemFlags
api_type:
- COM
ms.assetid: bb7ccb45-ce08-4d22-9259-db15cd267e34
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cae4ef6e4d7634ca2b429eb946aa948f5d90cd92
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19820426"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>Propiedad canónica PidTagToDoItemFlags

  
  
**Hace referencia a**: Outlook 
  
Representa la condición marcado del elemento de tareas pendientes.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Identificador:  <br/> |0x0E2B  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI no transmisible  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es un campo de bits en el que cada bit debe establecerse en 1 si se aplica la condición asociada en la tabla siguiente, en caso contrario, 0.
  
||||
|:-----|:-----|:-----|
|Valor numérico  <br/> |Nombre  <br/> |Descripción  <br/> |
|No está presente  <br/> |N/D  <br/> |Sin marca  <br/> |
|1  <br/> |todoTimeFlagged  <br/> |Objeto es marcada de hora  <br/> |
|8  <br/> |todoRecipientFlagged  <br/> |Sólo se debe establecer en un objeto de mensaje de borrador y significa que el objeto se marca para los destinatarios.  <br/> |
   
Se reservan todos los bits que no se especifican en la tabla. Debe omitirse, pero deben conservarse si se han establecido.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones relacionadas con marcas.
    
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

