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
ms.openlocfilehash: 053ec531f69ff7734872466b7a661beff3177b2c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348485"
---
# <a name="pidlidaddressbookprovideremaillist-canonical-property"></a>Propiedad canónica PidLidAddressBookProviderEmailList

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica qué propiedades de dirección electrónica se establecen en el contacto. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidABPEmailList  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Id. largo (LID):  <br/> |0x00008028  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Cada PT_LONG valor de esta propiedad debe ser único en la propiedad y debe establecerse en uno de los valores de la tabla siguiente. Si se establece esta propiedad, también se debe establecer la propiedad **dispidABPArrayType** ([PidLidAddressBookProviderArrayType](pidlidaddressbookproviderarraytype-canonical-property.md)). Estas dos propiedades deben mantenerse sincronizadas entre sí. Por ejemplo, si uno de los valores de **dispidABPEmailList** es "0x00000000", **dispidABPArrayType** debe tener el conjunto de bits "0x00000001". 
  
|**Valor**|**Descripción**|
|:-----|:-----|
|0x00000000  <br/> |Email1 se define para el contacto.  <br/> |
|0x00000001  <br/> |Email2 se define para el contacto.  <br/> |
|0x00000002  <br/> |Email3 se define para el contacto.  <br/> |
|0x00000003  <br/> |El fax de empresa se define para el contacto.  <br/> |
|0x00000004  <br/> |El fax principal se define para el contacto.  <br/> |
|0x00000005  <br/> |El fax principal se define para el contacto.  <br/> |
   
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

