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
  
Especifica cómo generar y volver a compilar el valor de la propiedad **dispidFileUnder** ([PidLidFileUnder](pidlidfileunder-canonical-property.md)) cuando cambian otras propiedades de nombre de contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidFileUnderId  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Id. largo (LID):  <br/> |0x00008006  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Si falta esta propiedad o se establece en un valor que no se detalla en la tabla siguiente o [en [MS-OXOCNTC],](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)la aplicación puede elegir su propia lógica para volver a compilar el valor de **dispidFileUnder** a medida que cambian otras propiedades de nombre de contacto. 
  
En la tabla siguiente, se usa la notación <PropertyName> para especificar "el valor de PropertyName". Por ejemplo, si el valor de la propiedad **PR_SURNAME** ([PidTagSurname](pidtagsurname-canonical-property.md)) es "Smith", y el valor de la propiedad **PR_GIVEN_NAME** ([PidTagGivenName](pidtaggivenname-canonical-property.md)) es "Ben", " " especifica la cadena <PidTagGivenName> <PidTagSurname> "Ben Smith". En la tabla, "\r" especifica un carácter de retorno de carro, "\n" especifica un carácter de fuente de línea y <space> representa un carácter de espacio.
  
|**Valor de la **propiedad dispidFileUnderId****|**Descripción de la **propiedad dispidFileUnder****|
|:-----|:-----|
|0x00000000  <br/> |Vacío PT_UNICODE.  <br/> |
|0x00003001  <br/> |" \< PidTagDisplayName \> "  <br/> |
|0x00003A06  <br/> |" \< PidTagGivenName \> "  <br/> |
|0x00003A11  <br/> |" \< PidTagSurname \> "  <br/> |
|0x00003A16  <br/> |" \< PidTagCompanyName \> "  <br/> |
|0x00008017  <br/> |" \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "  <br/> |
|0x00008018  <br/> |" \< PidTagCompanyName \>\r\n\< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName \> "  <br/> |
|0x00008019  <br/> |" \< PidTagSurname \> , space \< \> \< PidTagGivenName space \> \< \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "  <br/> |
|0x00008030  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "  <br/> |
|0x00008031  <br/> |" \< Espacio PidTagSurname \> \< \> \< PidTagGivenName \> \< espacio \> \< PidTagMiddleName \> "  <br/> |
|0x00008032  <br/> |" \< PidTagCompanyName \>\r\n\< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "  <br/> |
|0x00008033  <br/> |" \< PidTagCompanyName \>\r\n\< pidTagSurname \> \< space \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> "  <br/> |
|0x00008034  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \>\r\n\< PidTagCompanyName \> "  <br/> |
|0x00008035  <br/> |" \< Espacio PidTagSurname \> \< \> \< PidTagGivenName \> \< espacio \> \< PidTagMiddleName\r\n\> \< PidTagCompanyName \> "  <br/> |
|0x00008036  <br/> |" \< Espacio PidTagSurname \> \< \> \< PidTagGivenName \> \< espacio \> \< PidTagMiddleName espacio \> \< \> \< PidTagGeneration \> "  <br/> |
|0x00008037  <br/> |" \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \< space \> \< PidTagSurname space \> \< \> \< PidTagGeneration \> "  <br/> |
|0x00008038  <br/> |" \< PidTagSurname \> \< PidTagGivenName \> \< space \> \< PidTagMiddleName \> \< space \> \< PidTagGeneration \> "  <br/> |
|0xfffffffd  <br/> |Especifica que, al mostrar el contacto, la aplicación debe intentar usar el valor actual de **dispidFileUnder** y otras propiedades de contacto para encontrar una "mejor coincidencia" para **dispidFileUnderId** con uno de los valores anteriores de esta tabla.  <br/> |
|0xfffffffe  <br/> |Especifica que, al mostrar el contacto, la aplicación debe elegir los valores predeterminados adecuados (según la configuración regional de idioma) para **dispidFileUnderId** y actualizar **dispidFileUnder** para que coincida con la opción.  <br/> |
|0xffffffff  <br/> |**dispidFileUnder** es una propiedad proporcionada por PT_UNICODE y no debe cambiarse cuando cambie otra propiedad de nombre de contacto.  <br/> |
   
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

