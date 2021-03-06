---
title: Propiedad canónica PidTagPriority
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagPriority
api_type:
- COM
ms.assetid: 0f3a628f-5f8e-4716-98cc-868bd3400ba9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b9c0f5ebeae21d6d683bbb5def727d29a34bcdb6
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339434"
---
# <a name="pidtagpriority-canonical-property"></a>Propiedad canónica PidTagPriority

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la prioridad relativa de un mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PRIORITY  <br/> |
|Identificador:  <br/> |0x0026  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad y la **PR_IMPORTANCE** ([PidTagImportance](pidtagimportance-canonical-property.md)) no deben confundirse. Importance indica un valor para los usuarios, mientras que priority indica el orden o la velocidad a la que el software del sistema de mensajería debe enviar el mensaje. La prioridad más alta suele indicar un costo más alto. La interfaz de usuario suele asociar una mayor importancia a una pantalla diferente.
  
La prioridad de un mensaje de informe debe ser la misma que la prioridad del mensaje original que se va a notificar.
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
PRIO_NONURGENT 
  
> El mensaje no es urgente.
    
PRIO_NORMAL 
  
> El mensaje tiene prioridad normal.
    
PRIO_URGENT 
  
> El mensaje es urgente.
    
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas en objetos de mensaje de correo electrónico.
    
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

