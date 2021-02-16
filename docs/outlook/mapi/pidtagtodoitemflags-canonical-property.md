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
ms.openlocfilehash: 6ddc7231afef0a224b92be7fe86216e56200ab70
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32284486"
---
# <a name="pidtagtodoitemflags-canonical-property"></a>Propiedad canónica PidTagToDoItemFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa una To-Do marcada de un elemento.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_TODO_ITEM_FLAGS  <br/> |
|Identificador:  <br/> |0x0E2B  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |MAPI no transmitible  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es un campo de bits en el que cada bit debe establecerse en 1 si se aplica la condición asociada en la tabla siguiente; de lo contrario, 0.
  
||||
|:-----|:-----|:-----|
|Valor numérico  <br/> |Nombre  <br/> |Descripción  <br/> |
|No presente  <br/> |N/D  <br/> |Sin inflar  <br/> |
|1   <br/> |todoTimeFlagged  <br/> |El objeto está marcado por tiempo  <br/> |
|8   <br/> |todoRecipientFlagged  <br/> |Solo debe establecerse en un objeto de borrador de mensaje, lo que significa que el objeto está marcado para los destinatarios.  <br/> |
   
Se reservan todos los bits que no se especifican en la tabla. Deben omitirse, pero deben conservarse si se establecen.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones relacionadas con la marcación.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

