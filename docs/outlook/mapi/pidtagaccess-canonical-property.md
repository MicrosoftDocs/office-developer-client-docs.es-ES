---
title: Propiedad canónica PidTagAccess
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316516"
---
# <a name="pidtagaccess-canonical-property"></a>Propiedad canónica PidTagAccess

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de marcas que indica las operaciones que están disponibles para el cliente para el objeto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ACCESS  <br/> |
|Identificador:  <br/> |0x0FF4  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Propiedades del control de acceso  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad es de solo lectura para el cliente. Debe ser un or bit **a** bit de cero o más valores de la tabla siguiente. 
  
|**Name**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |Escritura  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Lectura  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |Eliminar  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |Crear subcarpetas en la jerarquía de carpetas  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |Crear mensajes de contenido  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |Crear mensajes de contenido asociados  <br/> |
   
Las marcas MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY y MAPI_ACCESS_READ se encuentran en los objetos de carpeta y mensaje, y en la columna **PR_ACCESS** de las tablas de contenido y las tablas de contenido asociadas. Las MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS y MAPI_ACCESS_CREATE_HIERARCHY se encuentran únicamente en objetos de carpeta. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y datos adjuntos.
    
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

