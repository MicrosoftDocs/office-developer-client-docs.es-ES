---
title: Propiedad canónica PidTagRoamingDatatypes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384265"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>Propiedad canónica PidTagRoamingDatatypes

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits que indica qué secuencia de propiedades que existen en el mensaje.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|Identificador:  <br/> |0x7C06  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Configuración  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad debe establecerse en uno o varios de los siguientes valores:
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000002  <br/> |Indica que el mensaje de la carpeta asociada información (FAI) debe contener una secuencia de diccionario, serializa en un esquema XML fijo y almacena en la propiedad **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)). Si el mensaje FAI no contiene una secuencia de diccionario, la aplicación debe tratar el diccionario como no tener ninguna entrada.  <br/> |
|0 x 00000004  <br/> |Indica que el mensaje FAI debe contener una secuencia XML que se almacena en la propiedad **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) que utiliza un esquema XML arbitrario.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica la ubicación y las propiedades de datos de configuración de cliente y servidor, como las listas de categoría compartida y horas de trabajo.
    
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

