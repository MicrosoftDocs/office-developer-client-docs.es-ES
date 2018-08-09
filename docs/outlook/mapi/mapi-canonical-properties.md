---
title: Propiedades MAPI canónicas
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2a080b9e6a824e50648a6df0757826f45b5da1f2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19818090"
---
# <a name="mapi-canonical-properties"></a>Propiedades MAPI canónicas

  
  
**Hace referencia a**: Outlook 
  
Una propiedad canónica es una propiedad virtual que representa una propiedad MAPI o varias propiedades MAPI definidas con el mismo identificador de propiedad. Propiedades canónicas sólo están diseñadas para facilitar la identificación coherente de las propiedades MAPI en discusiones o documentación fuera del código. A diferencia de los nombres de propiedades con etiqueta definidas en MAPI, los nombres de propiedad canónico no se definen como constantes globales en archivos de encabezado MAPI.
  
## <a name="naming-conventions"></a>Convenciones de nomenclatura

Los nombres de propiedad canónico comienzan con un prefijo, "Pid", que representa "identificador de la propiedad". Dependiendo de si la propiedad es una propiedad con etiqueta, una propiedad con nombre con un identificador numérico o una propiedad con nombre con un nombre de cadena, el prefijo aún más está calificado como "PidTag", "PidLid" y "PidName", respectivamente. Por ejemplo, [PidTagAccount](pidtagaccount-canonical-property.md) representa las propiedades con etiqueta, **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) y **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)), que especifican un destinatario nombre de cuenta; [PidLidContacts](pidlidcontacts-canonical-property.md) representa la propiedad **dispidContacts** , una propiedad con nombre que tiene un identificador numérico y que especifica el nombre de los contactos asociados con un mensaje; y [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) representa "http://schemas.microsoft.com/outlook/phishingstamp," una propiedad con nombre que tiene un nombre de cadena, y que especifica la cadena de marcado de mensajes que están probables que sean de suplantación de identidad. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Que representa las propiedades Similar mediante una propiedad canónica

### <a name="identifying-properties-in-mapi"></a>Identificación de las propiedades de MAPI

Todas las propiedades de MAPI se identifican mediante un identificador de propiedad que es un valor de 16 bits sin signo. Identificador de la propiedad y el tipo de propiedad (otro valor de 16 bits sin signo) constituyen una etiqueta de propiedad para la propiedad. 
  
MAPI utiliza una etiqueta de propiedad para definir las propiedades de forma exclusiva. Las propiedades que tienen la misma etiqueta de propiedad, como **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) y **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)), se consideran idénticas propiedades de MAPI. Para obtener una lista de etiquetas de propiedad que ha definido MAPI para sus propias propiedades, consulte el archivo de encabezado MAPI, Mapitags.h.
  
Tenga en cuenta que MAPI divide los identificadores de propiedades en intervalos. Donde se encuentra un identificador en el intervalo indica su uso y la propiedad. Los identificadores de propiedad de propiedades con etiqueta se dividen en el intervalo de 0 x 0001 a 0x7FFF. Dentro de este intervalo son los identificadores de propiedad de propiedades definidas por el MAPI, que se dividen en el intervalo de 0 x 0001 a 0x3FFF. Los identificadores de propiedad de la reversión de propiedades con nombre en el rango de 0 x 8000 a 0x8FFF. 
  
Propiedades con nombre se expresarán además por un conjunto de propiedades y un long identificador (tapa), que es un valor de 32 bits sin signo, o bien una cadena. Un conjunto de propiedades es un GUID que identifica un grupo de propiedades con nombre con un propósito similar. El conjunto de propiedades y el nombre de cubierta o cadena se usan para obtener o establecer la propiedad con nombre.
  
### <a name="property-type"></a>Tipo de propiedad

Aparte de los identificadores, se expresarán una propiedad con un tipo de datos que especifica el tipo de valores permitidos para esa propiedad.
  
Para las propiedades que son del tipo de cadena, dependiendo de la compatibilidad con Unicode en la plataforma subyacente, la propiedad puede ser de tipo PT_STRING8 (cadena de caracteres terminada en null de 8 bits) o PT_UNICODE (cadena Unicode terminada en null). Se puede definir una propiedad con el tipo de PT_TSTRING y, según la configuración de la compilación, PT_TSTRING el valor predeterminado es a una cadena Unicode para plataformas que admiten Unicode o en una cadena PT_STRING8 para plataformas que admiten ANSI o DBCS. Es habitual que una propiedad de tipo cadena es identificado por tres nombres similares, como **PR_ACCOUNT**, **PR_ACCOUNT_A**y **PR_ACCOUNT_W**, que son del tipo PT_TSTRING, PT_STRING8 y PT_UNICODE respectivamente.
  
Para obtener más información sobre los tipos de propiedad y relacionadas con los tipos de macros, vea el archivo de encabezado MAPI, Mapidefs.h.
  
### <a name="identifying-similar-properties"></a>Identificación de propiedades similares

En el panorama actual de la propiedad MAPI, no es frecuente encontrar que se ha expuesto una propiedad en nombres de propiedad diferentes, todos los cuales se definen con el mismo identificador de propiedad. Por ejemplo, las propiedades con etiqueta, **PR_BUSINESS2_TELEPHONE_NUMBER** y **PR_OFFICE2_TELEPHONE_NUMBER**, se definen en Mapitags.h tengan el mismo identificador de la propiedad y el tipo. Estrechamente relacionadas con estas dos propiedades son:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Las propiedades con el sufijo "_A" se escriben como PT_STRING8 y aquellos con el sufijo "_W" se escriben como PT_UNICODE.
  
Es el propósito de una propiedad canónico, **PidTagBusiness2TelephoneNumber** en este ejemplo facilitar la referencia a dichas propiedades MAPI afiliadas estrechamente con un identificador y de una manera coherente (con el prefijo "Pid") a través de todos los MAPI Propiedades. Para averiguar qué propiedades MAPI reales que representa una propiedad canónica, vea [Asignación de nombres de propiedad canónico a nombres de MAPI](mapping-canonical-property-names-to-mapi-names.md). Para buscar la propiedad canónica que está asociada una propiedad MAPI, vea [Asignación de nombres de MAPI para los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md).
  
## <a name="mapi-support-of-canonical-property-names"></a>Compatibilidad con MAPI de nombres canónicos (propiedad)

Debido a que las propiedades canónicas no son propiedades real y no están definidas en los archivos de encabezado MAPI, no deben usar los nombres de propiedad canónico en el código. en su lugar, deberían seguir usar los nombres de propiedad MAPI exactos en el código. Por ejemplo, se puede hacer referencia **PR_BUSINESS2_TELEPHONE_NUMBER** y **PR_OFFICE2_TELEPHONE_NUMBER** fuera del código como **PidTagBusiness2TelephoneNumber**y usar **PR_BUSINESS2_TELEPHONE_NUMBER** o **PR_OFFICE2_ TELEPHONE_NUMBER** en el código. 
  
Si debe usar nombres canónicos (propiedad) en el código, primero debe definir ellos en sus propios archivos de encabezado.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Nombres de propiedad canónico y las especificaciones de protocolo de Exchange

Nombres canónicos se hace referencia en las especificaciones de protocolo de Microsoft Exchange Server que se utilizan para comunicarse con otros productos de Microsoft Exchange Server. Para obtener más información acerca de las propiedades de objeto de mensaje hace referencia a las especificaciones de protocolo de Exchange, vea [[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Vea también



[Etiquetas MAPI (propiedad)](mapi-property-tags.md)
  
[Información general sobre el identificador de propiedad MAPI](mapi-property-identifier-overview.md)
  
[Información general sobre el tipo de propiedad MAPI](mapi-property-type-overview.md)

