---
title: Propiedad canónica PidNameContentClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidNameContentClass
api_type:
- COM
ms.assetid: 6f623345-b30e-452f-a822-9308b455697a
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 51788a49d1c0d01ef7ff5daca853000a8f1e34a0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356353"
---
# <a name="pidnamecontentclass-canonical-property"></a>Propiedad canónica PidNameContentClass

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene un valor de campo de encabezado de clase de contenido [RFC3282].
  
|||
|:-----|:-----|
|Nombres descriptivos:  <br/> |Ninguno  <br/> |
|Conjunto de propiedades:  <br/> |PS_INTERNET_HEADERS  <br/> |
|Nombre de la propiedad:  <br/> |Content-Class  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Para establecer el valor de esta propiedad, los clientes de Extensiones multipropósito a mensajes de Internet (MIME) deben escribir un campo de encabezado Content-Class con el valor deseado. Los lectores MIME deben copiar el valor de un campo de encabezado Content-Class en el valor de esta propiedad. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Convierte las convenciones de correo electrónico estándar de Internet en objetos de mensaje.
    
[[MS-OXORMMS]](https://msdn.microsoft.com/library/a121dda4-48f3-41f8-b12f-170f533038bb%28Office.15%29.aspx)
  
> Especifica las propiedades de los mensajes codificados con derechos administrados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

