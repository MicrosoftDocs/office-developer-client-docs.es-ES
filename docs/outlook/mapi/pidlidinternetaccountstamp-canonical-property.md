---
title: Propiedad canónica PidLidInternetAccountStamp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidInternetAccountStamp
api_type:
- COM
ms.assetid: 819179fe-e58e-415c-abc7-1949036745ee
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ebd64392d24cd170a7babf77865aa00c7be24802
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315459"
---
# <a name="pidlidinternetaccountstamp-canonical-property"></a>Propiedad canónica PidLidInternetAccountStamp

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el identificador de cuenta de correo electrónico a través del cual se envía el mensaje de correo electrónico.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidInetAcctStamp  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Id. largo (LID):  <br/> |0x00008581  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Mensajería general  <br/> |
   
## <a name="remarks"></a>Comentarios

El formato de esta cadena depende de la implementación. El cliente puede usar esta propiedad para determinar a qué servidor dirigir el correo, pero es opcional y el valor no tiene ningún significado para el servidor.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona la definición del conjunto de propiedades y las referencias a las Exchange Server de protocolo relacionados.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones que son permisibles para los objetos de mensaje de correo electrónico.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

