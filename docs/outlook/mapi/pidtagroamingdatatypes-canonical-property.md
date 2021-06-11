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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359559"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>Propiedad canónica PidTagRoamingDatatypes

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits que indica qué propiedades de secuencia existen en el mensaje.
  
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
|0x00000002  <br/> |Indica que el mensaje Folder Associated Information (FAI) debe contener una secuencia Dictionary, serializada en un esquema XML fijo y almacenada en la propiedad **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)). Si el mensaje FAI no contiene una secuencia Dictionary, la aplicación debe tratar el Dictionary como que no tiene entradas.  <br/> |
|0x00000004  <br/> |Indica que el mensaje FAI debe contener una secuencia XML almacenada en la propiedad **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)) que usa un esquema XML arbitrario.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica la ubicación y las propiedades de los datos de configuración de cliente y servidor, como listas de categorías compartidas y horas laborables.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

