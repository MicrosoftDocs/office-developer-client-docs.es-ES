---
title: Propiedad canónica PidLidAddressBookProviderArrayType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidAddressBookProviderArrayType
api_type:
- COM
ms.assetid: ca4eb6c2-98e9-4dbc-9f5a-f0f257456ead
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 68396f210aab465da9cec4a74a3c24cc4e8578a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348443"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>Propiedad canónica PidLidAddressBookProviderArrayType

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica el estado de las direcciones electrónicas del contacto y representa un conjunto de marcas de bits.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidABPArrayType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Id. largo (LID):  <br/> |0x00008029  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de la **propiedad dispidABPArrayType** debe ser una combinación de marcas que especifiquen el estado del objeto de contacto. Las marcas individuales se especifican en la tabla siguiente. Si se establece esta propiedad, también se debe establecer la propiedad **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)). Estas dos propiedades deben mantenerse sincronizadas entre sí. Por ejemplo, si **dispidABPArrayType** tiene el bit "0x00000001 set", uno de los valores de **dispidABPEmailList** debe ser "0x00000000". 
  
|**Bit**|**Descripción**|
|:-----|:-----|
|0x00000001  <br/> |Email1 se define para el contacto.  <br/> |
|0x00000002  <br/> |Email2 se define para el contacto.  <br/> |
|0x00000004  <br/> |Email3 se define para el contacto.  <br/> |
|0x00000008  <br/> |El fax de empresa se define para el contacto.  <br/> |
|0x00000010  <br/> |El fax principal se define para el contacto.  <br/> |
|0x00000020  <br/> |El fax principal se define para el contacto.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

