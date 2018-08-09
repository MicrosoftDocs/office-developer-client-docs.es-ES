---
title: Propiedad canónica PidLidAddressBookProviderEmailList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderEmailList
api_type:
- COM
ms.assetid: 9c0527ea-e922-4514-b913-d3520350c452
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 4eb2897c1834715f3d937ef7946998943b386aef
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818488"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>Propiedad canónica PidLidAddressBookProviderEmailList

  
  
**Hace referencia a**: Outlook 
  
Especifica qué propiedades de dirección electrónica se establecen en el contacto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidABPEmailList  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008028  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Cada valor PT_LONG en esta propiedad debe ser único en la propiedad y debe establecerse en uno de los valores en la tabla siguiente. Si se establece esta propiedad, también se debe establecer la propiedad **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)). Estas dos propiedades se deben mantener sincronizadas con cada una de las demás. Por ejemplo, si uno de los valores de **dispidABPEmailList** es "0 x 00000000" y, a continuación, **dispidABPArrayType** debe haber establecido el bit "0 x 00000001". 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |Correo electrónico1 se define para el contacto.  <br/> |
|0x00000001  <br/> |Correo electrónico 2 se define para el contacto.  <br/> |
|0x00000002  <br/> |Correo electrónico 3 se define para el contacto.  <br/> |
|0 x 00000003  <br/> |Fax del trabajo se define para el contacto.  <br/> |
|0 x 00000004  <br/> |Fax del domicilio particular se define para el contacto.  <br/> |
|0 x 00000005  <br/> |Fax principal se define para el contacto.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

