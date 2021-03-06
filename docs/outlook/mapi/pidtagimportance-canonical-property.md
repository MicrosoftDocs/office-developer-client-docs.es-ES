---
title: Propiedad canónica PidTagImportance
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagImportance
api_type:
- HeaderDef
ms.assetid: 274dd444-a863-4b53-bdbc-3763c375c43c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6bef8b05f2fbf94b74ee126b80dfc6ae0c5e9d11
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327926"
---
# <a name="pidtagimportance-canonical-property"></a>Propiedad canónica PidTagImportance

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor que indica la opinión del remitente del mensaje sobre la importancia de un mensaje. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_IMPORTANCE  <br/> |
|Identificador:  <br/> |0x0017  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad y **la PR_PRIORITY** ([PidTagPriority](pidtagpriority-canonical-property.md)) no deben confundirse. Importance indica un valor para los usuarios, mientras que priority indica el orden o la velocidad a la que el software del sistema de mensajería debe enviar el mensaje. La prioridad más alta suele indicar un costo más alto. La interfaz de usuario suele asociar una mayor importancia a una pantalla diferente. 
  
Esta propiedad puede tener exactamente uno de los siguientes valores:
  
IMPORTANCE_LOW 
  
> El mensaje tiene poca importancia.
    
IMPORTANCE_HIGH 
  
> El mensaje tiene una gran importancia.
    
IMPORTANCE_NORMAL 
  
> El mensaje tiene una importancia normal.
    
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

