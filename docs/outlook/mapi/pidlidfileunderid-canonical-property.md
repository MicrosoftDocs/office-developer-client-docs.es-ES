---
title: Propiedad canónica PidLidFileUnderId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFileUnderId
api_type:
- COM
ms.assetid: 917431a9-fd90-4b4d-b042-886e3dbf47c0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 08e2403be35b87393d22f9109f59c0572c53073b
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818744"
---
# <a name="pidlidfileunderid-canonical-property"></a>Propiedad canónica PidLidFileUnderId

  
  
**Hace referencia a**: Outlook 
  
Especifica cómo se debe generar y volver a calcular el valor de la propiedad **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) al cambio de las propiedades nombre a otros contactos.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidFileUnderId  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008006  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Si esta propiedad se falta o se establece en un valor no detallado en la tabla siguiente o en [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), la aplicación puede elegir su propia lógica para volver a calcular el valor de la **dispidFileUnder** como otro cambio de las propiedades nombre del contacto. 
  
En la siguiente tabla, la notación <PropertyName> se usa para especificar "el valor de PropertyName". Por ejemplo, si el valor de la propiedad **PR_SURNAME** ([pidtagsurname MAPI](pidtagsurname-canonical-property.md)) es "Smith", y el valor de la propiedad **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) es "Ben", a continuación, "<PidTagGivenName> <PidTagSurname>" especifica la cadena "Ben Smith". En la tabla, "\r" especifica un carácter de retorno de carro, "\n" especifica un carácter de salto de línea, y <space> representa un carácter de espacio.
  
|**Valor de la propiedad **dispidFileUnderId****|**Descripción de la propiedad **dispidFileUnder****|
|:-----|:-----|
|0x00000000  <br/> |PT_UNICODE vacía.  <br/> |
|0x00003001  <br/> |"\<PidTagDisplayName\>"  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>"  <br/> |
|0x00003A11  <br/> |"\<Pidtagsurname MAPI\>"  <br/> |
|0x00003A16  <br/> |"\<PidTagCompanyName\>"  <br/> |
|0x00008017  <br/> |"\<Pidtagsurname MAPI\>,\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"  <br/> |
|0x00008018  <br/> |"\<PidTagCompanyName\>\r\n\<pidtagsurname MAPI\>,\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"  <br/> |
|0x00008019  <br/> |"\<Pidtagsurname MAPI\>,\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008030  <br/> |"\<Pidtagsurname MAPI\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"  <br/> |
|0x00008031  <br/> |"\<Pidtagsurname MAPI\>\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"  <br/> |
|0x00008032  <br/> |"\<PidTagCompanyName\>\r\n\<pidtagsurname MAPI\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"  <br/> |
|0x00008033  <br/> |"\<PidTagCompanyName\>\r\n\<pidtagsurname MAPI\>\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>"  <br/> |
|0x00008034  <br/> |"\<Pidtagsurname MAPI\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008035  <br/> |"\<Pidtagsurname MAPI\>\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\r\n\<PidTagCompanyName\>"  <br/> |
|0x00008036  <br/> |"\<Pidtagsurname MAPI\>\<espacio\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\<espacio\>\<PidTagGeneration\>"  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\<espacio\>\<pidtagsurname MAPI\>\<espacio\>\<PidTagGeneration\>"  <br/> |
|0x00008038  <br/> |"\<Pidtagsurname MAPI\>\<PidTagGivenName\>\<espacio\>\<PidTagMiddleName\>\<espacio\>\<PidTagGeneration\>"  <br/> |
|0xfffffffd  <br/> |Especifica que, cuando se muestra el contacto, la aplicación debe intentar usar el valor actual de **dispidFileUnder** y otras propiedades de contacto para buscar a una "mejor coincidencia" para **dispidFileUnderId** a uno de los valores anteriores de esta tabla.  <br/> |
|0xFFFFFFFE  <br/> |Especifica que, cuando se muestra el contacto, la aplicación debe elegir los valores predeterminados adecuados (de acuerdo con la configuración regional de idioma) para **dispidFileUnderId** y **dispidFileUnder** para que coincida con la opción de actualización.  <br/> |
|0xFFFFFFFF  <br/> |**dispidFileUnder** es un PT_UNICODE proporcionado por el usuario y no se debe cambiar cuando cambia de otra propiedad de nombre del contacto.  <br/> |
   
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

