---
title: Propiedad canónica PidTagAdditionalRenEntryIds
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIds
api_type:
- HeaderDef
ms.assetid: 8c6e7ca2-1824-4cca-bf69-3c1ea52727de
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4984055d370f3f8ab617b11b2d834ba277ef105a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32282364"
---
# <a name="pidtagadditionalrenentryids-canonical-property"></a>Propiedad canónica PidTagAdditionalRenEntryIds

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene los identificadores de entrada de algunas carpetas especiales. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS  <br/> |
|Identificador:  <br/> |0x36D8  <br/> |
|Tipo de datos:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Aplicación de Outlook  <br/> |
   
## <a name="remarks"></a>Comentarios

Las cinco primeras entradas de esta propiedad de varios valores se aplican a las siguientes carpetas especiales, si existen en la tienda:
  
0: carpeta conflictos
  
1-carpeta problemas de sincronización
  
2-carpeta errores locales
  
carpeta de errores de 3 servidores
  
4-carpeta de correo no deseado
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para crear y ubicar las carpetas especiales en un buzón.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Identifica y marca los mensajes de correo electrónico diseñados para engañar a los destinatarios para que divulguen información confidencial (como contraseñas y otra información personal) a un origen que no es de confianza.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Habilita el control de las listas de permitidos y bloqueados y la determinación de los mensajes de correo electrónico no deseado.
    
### <a name="header-files"></a>Archivos de encabezado

Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)


[Información sobre la API del almacén](https://msdn.microsoft.com/library/aa192884.aspx)

