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
ms.openlocfilehash: 7af30866a5fd2846327223b7a58c6de91f5fef7a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355709"
---
# <a name="pidlidfileunderid-canonical-property"></a>Propiedad canónica PidLidFileUnderId

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica cómo generar y volver a calcular el valor de la propiedad **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) cuando cambian las propiedades de otros nombres de contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidFileUnderId  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|IDENTIFICADOR largo (LID):  <br/> |0x00008006  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contact  <br/> |
   
## <a name="remarks"></a>Comentarios

Si esta propiedad falta o se establece en un valor no detallado en la tabla siguiente o en [[ms-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx), la aplicación puede elegir su propia lógica para volver a calcular el valor de **dispidFileUnder** como cambios en las propiedades de otros nombres de contacto. 
  
En la tabla siguiente, la notación <PropertyName> se usa para especificar "el valor de PropertyName". Por ejemplo, si el valor de la propiedad **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) es "Smith" y el valor de la propiedad **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) es "Ben", entonces "<PidTagGivenName> <PidTagSurname>" especifica la cadena "Miguel Saavedra". En la tabla, "\r" especifica un carácter de retorno de carro, "\n" especifica un carácter de salto de <space> línea y representa un carácter de espacio.
  
|**Valor de la propiedad **dispidFileUnderId****|**Descripción de la propiedad **dispidFileUnder****|
|:-----|:-----|
|0x00000000  <br/> |PT_UNICODE vacío.  <br/> |
|0x00003001  <br/> |"\<PidTagDisplayName\>"  <br/> |
|0x00003A06  <br/> |"\<PidTagGivenName\>"  <br/> |
|0x00003A11  <br/> |"\<PidTagSurname\>"  <br/> |
|0x00003A16  <br/> |"\<PidTagCompanyName\>"  <br/> |
|0x00008017  <br/> |"\<PidTagSurname\>,\<Space\>\<PidTagGivenName\>\<Space\>"\<\>  <br/> |
|0x00008018  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>,\<espacio\>\<PidTagGivenName\>\<espacio\>"\<\>  <br/> |
|0x00008019  <br/> |"\<PidTagSurname\>,\<espacio\>\<PidTagGivenName\>\>espacio PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<  <br/> |
|0x00008030  <br/> |"\<PidTagSurname\>\<\>PidTagGivenName\<espacio\>PidTagMiddleName\>"\<  <br/> |
|0x00008031  <br/> |"\<PidTagSurname\>\<espacio\>\>\<en PidTagGivenName\>espacio en PidTagMiddleName\>"\<\<  <br/> |
|0x00008032  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<PidTagGivenName\>\<espacio\>"\<\>  <br/> |
|0x00008033  <br/> |"\<PidTagCompanyName\>\r\n\<PidTagSurname\>\<espacio\>\>PidTagGivenName\<PidTagMiddleName\>\<\<\>  <br/> |
|0x00008034  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\>espacio PidTagMiddleName\>\r\n\<PidTagCompanyName\>"\<\<  <br/> |
|0x00008035  <br/> |"\<PidTagSurname\>\<espacio\>\>\>en PidTagGivenName\<\>espacio PidTagMiddleName\>\r\n\<PidTagCompanyName"\<\<  <br/> |
|0x00008036  <br/> |"\<PidTagSurname\>\>\<\>\<\<espacio en PidTagGivenName\>\>espacio en\<PidTagMiddleName\>de espacio en\>\<\<  <br/> |
|0x00008037  <br/> |"\<PidTagGivenName\>\>\<\>\<\<espacio en PidTagMiddleName\>\>espacio en\<PidTagSurname\>de espacio en\>\<\<  <br/> |
|0x00008038  <br/> |"\<PidTagSurname\>\<PidTagGivenName\>\<espacio\>PidTagMiddleName\>PidTagGeneration"\<\>\<\<\>  <br/> |
|0xfffffffd  <br/> |Especifica que, al mostrar el contacto, la aplicación debe intentar usar el valor actual de **dispidFileUnder** y otras propiedades de contacto para encontrar una "mejor coincidencia" para **dispidFileUnderId** a uno de los valores anteriores de esta tabla.  <br/> |
|0xFFFFFFFE  <br/> |Especifica que, al mostrar el contacto, la aplicación debe elegir los valores predeterminados adecuados (de acuerdo con la configuración regional de idioma) para **dispidFileUnderId** y actualizar **dispidFileUnder** para que coincida con la opción.  <br/> |
|0xFFFFFFFF  <br/> |**dispidFileUnder** es un PT_UNICODE proporcionado por el usuario y no debe cambiarse cuando otra propiedad de nombre de contacto cambia.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se admiten para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

