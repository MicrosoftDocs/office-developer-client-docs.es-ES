---
title: Propiedades canónicas de MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 4b017089a675727703de9e2ed4d584e7f77a778a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319057"
---
# <a name="mapi-canonical-properties"></a>Propiedades canónicas de MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una propiedad canónica es una propiedad virtual que representa una propiedad MAPI o varias propiedades MAPI definidas con el mismo identificador de propiedad. Las propiedades canónicas solo están destinadas a facilitar la identificación coherente de las propiedades MAPI en discusiones o documentación fuera del código. A diferencia de los nombres de propiedad etiquetada definidos por MAPI, los nombres de propiedad canónicos no se definen como constantes globales en los archivos de encabezado MAPI.
  
## <a name="naming-conventions"></a>Convenciones de nomenclatura

Los nombres de propiedad canónica comienzan con un prefijo, "PID", que representa "identificador de propiedad". Dependiendo de si la propiedad es una propiedad etiquetada, una propiedad con nombre con un identificador numérico o una propiedad con nombre con un nombre de cadena, el prefijo se califica con más precisión como "PidTag", "PidLid" y "PidName", respectivamente. Por ejemplo, [PidTagAccount](pidtagaccount-canonical-property.md) representa las propiedades etiquetadas, **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)) **, PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) y **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)), que especifican el de un destinatario. nombre de la cuenta; [PidLidContacts](pidlidcontacts-canonical-property.md) representa la propiedad **dispidContacts** , una propiedad con nombre que tiene un identificador numérico y que especifica el nombre de los contactos asociados a un mensaje; y [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) representa "https://schemas.microsoft.com/outlook/phishingstamp," una propiedad con nombre que tiene un nombre de cadena y que especifica la cadena que es probable que sea la suplantación de identidad. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Representación de propiedades similares mediante una propiedad canónica

### <a name="identifying-properties-in-mapi"></a>Identificación de propiedades en MAPI

Todas las propiedades de MAPI se identifican mediante un identificador de propiedad que es un valor de 16 bits sin signo. El identificador de propiedad y el tipo de propiedad (otro valor de 16 bits sin signo) constituyen una etiqueta de propiedad para la propiedad. 
  
MAPI usa una etiqueta de propiedad para definir las propiedades de manera única. Las propiedades que tienen la misma etiqueta de propiedad, como **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) y **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)), se consideran idénticas propiedades en MAPI. Para obtener una lista de las etiquetas de propiedad que MAPI ha definido para sus propias propiedades, vea el archivo de encabezado MAPI Mapitags. h.
  
Tenga en cuenta que MAPI divide los identificadores de propiedad en rangos. Donde un identificador cae en el intervalo indica su uso y propiedad. Los identificadores de propiedad de las propiedades etiquetadas se sitúan en el intervalo de 0x0001 a 0x7FFF. Dentro de este intervalo se encuentran los identificadores de propiedad de las propiedades definidas por MAPI, que se encuentran en el intervalo de 0x0001 a 0x3FFF. Los identificadores de propiedad de las propiedades con nombre se encuentran en el intervalo de 0x8000 a 0x8FFF. 
  
Las propiedades con nombre también son atribuidas por un conjunto de propiedades, y ya sea un identificador largo (LID), que es un valor de 32 bits sin signo o una cadena. Un conjunto de propiedades es un GUID que identifica un grupo de propiedades con nombre con un propósito similar. El conjunto de propiedades y el nombre de la tapa o la cadena se usan para obtener o establecer la propiedad con nombre.
  
### <a name="property-type"></a>Tipo de propiedad

Aparte de los identificadores, una propiedad es atribuida por un tipo de datos que especifica el tipo de valores permitidos para esa propiedad.
  
Para las propiedades que son del tipo cadena, en función de la compatibilidad con Unicode en la plataforma subyacente, la propiedad puede ser del tipo PT_STRING8 (cadena de caracteres de 8 bits terminada en null) o PT_UNICODE (cadena Unicode terminada en null). Se puede definir una propiedad con el tipo PT_TSTRING y, en función de la configuración de compilación, PT_TSTRING utiliza de forma predeterminada una cadena Unicode para plataformas compatibles con Unicode, o una cadena de PT_STRING8 para plataformas compatibles con ANSI o DBCS. Es habitual que una propiedad de tipo cadena se identifique con tres nombres similares, como **PR_ACCOUNT**, **PR_ACCOUNT_A**y **PR_ACCOUNT_W**, que son del tipo PT_TSTRING, PT_STRING8 y PT_UNICODE, respectivamente.
  
Para obtener más información sobre los tipos de propiedades y las macros relacionadas con los tipos, vea el archivo de encabezado MAPI Mapidefs. h.
  
### <a name="identifying-similar-properties"></a>Identificación de propiedades similares

En la horizontal de la propiedad MAPI actual, no es raro encontrar que una propiedad se ha expuesto en nombres de propiedad diferentes, todos ellos definidos con el mismo identificador de propiedad. Por ejemplo, las propiedades etiquetadas, **PR_BUSINESS2_TELEPHONE_NUMBER** y **PR_OFFICE2_TELEPHONE_NUMBER**, se definen en Mapitags. h para tener el mismo identificador de propiedad y tipo. Estas dos propiedades están estrechamente relacionadas con las siguientes:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Las propiedades con el sufijo "_A" se escriben como PT_STRING8 y las que tienen el sufijo "_W" se escriben como PT_UNICODE.
  
El propósito de una propiedad canónica, <b0>PidTagBusiness2TelephoneNumber</b0> en este ejemplo, es facilitar la referencia a las propiedades MAPI estrechamente ligadas mediante un identificador y de manera coherente (con el prefijo "PID") en todos los MAPI </a1>. Para averiguar qué propiedades MAPI reales representa una propiedad canónica, consulte [asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md). Para buscar la propiedad canónica a la que está asociada una propiedad MAPI, vea [asignar nombres MAPI a nombres de propiedad canónica](mapping-mapi-names-to-canonical-property-names.md).
  
## <a name="mapi-support-of-canonical-property-names"></a>Compatibilidad con MAPI de nombres de propiedades canónicas

Dado que las propiedades canónicas no son propiedades reales y no están definidas en los archivos de encabezado MAPI, no debe usar nombres de propiedad canónicos en el código; en su lugar, debe seguir usando los nombres de propiedades MAPI exactas en el código. Por ejemplo, puede hacer referencia a **PR_BUSINESS2_TELEPHONE_NUMBER** y **PR_OFFICE2_TELEPHONE_NUMBER** fuera del código como **PidTagBusiness2TelephoneNumber**y usar **PR_BUSINESS2_TELEPHONE_NUMBER** o **PR_OFFICE2_ TELEPHONE_NUMBER** en el código. 
  
Si debe usar nombres de propiedad canónicos en el código, primero debe definirlos en sus propios archivos de encabezado.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Nombres de propiedad canónicos y especificaciones del Protocolo de Exchange

En las especificaciones del protocolo Microsoft Exchange Server, se hace referencia a nombres canónicos que usa Exchange Server para comunicarse con otros productos de Microsoft. Para obtener más información acerca de las propiedades de objetos de mensaje a las que hacen referencia las especificaciones del Protocolo de Exchange, consulte [[ms-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Vea también



[Etiquetas de propiedad MAPI](mapi-property-tags.md)
  
[Información general del identificador de propiedad MAPI](mapi-property-identifier-overview.md)
  
[Información general del tipo de propiedad MAPI](mapi-property-type-overview.md)

