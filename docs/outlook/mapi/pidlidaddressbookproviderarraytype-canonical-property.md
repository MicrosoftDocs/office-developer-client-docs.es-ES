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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393092"
---
# <a name="pidlidaddressbookproviderarraytype-canonical-property"></a>Propiedad canónica PidLidAddressBookProviderArrayType

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica el estado de las direcciones de presentación electrónica del contacto y representa un conjunto de indicadores de bits.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidABPArrayType  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008029  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor de la propiedad **dispidABPArrayType** debe ser una combinación de marcadores que especifican el estado del objeto de contacto. Indicadores individuales se especifican en la siguiente tabla. Si se establece esta propiedad, la propiedad **dispidABPEmailList** ([PidLidAddressBookProviderEmailList](pidlidaddressbookprovideremaillist-canonical-property.md)) debe establecerse, así como. Estas dos propiedades se deben mantener sincronizadas con cada una de las demás. Por ejemplo, si **dispidABPArrayType** tiene el bit "0 x 00000001 conjunto", uno de los valores de **dispidABPEmailList** debe ser "0 x 00000000". 
  
|**Bit**|**Descripción**|
|:-----|:-----|
|0x00000001  <br/> |Correo electrónico1 se define para el contacto.  <br/> |
|0x00000002  <br/> |Correo electrónico 2 se define para el contacto.  <br/> |
|0 x 00000004  <br/> |Correo electrónico 3 se define para el contacto.  <br/> |
|0 x 00000008  <br/> |Fax del trabajo se define para el contacto.  <br/> |
|0 x 00000010  <br/> |Fax del domicilio particular se define para el contacto.  <br/> |
|0 x 00000020  <br/> |Fax principal se define para el contacto.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

