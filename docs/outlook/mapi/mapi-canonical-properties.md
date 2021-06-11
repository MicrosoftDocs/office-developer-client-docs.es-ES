---
title: Propiedades canónicas MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 29151beb-7436-401a-8072-58d4facd8458
description: 'Última modificación: 23 de julio de 2011'
ms.openlocfilehash: 2fc605c57936765f43d7a6941dcc8d40d058db2f
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 05/29/2019
ms.locfileid: "34540479"
---
# <a name="mapi-canonical-properties"></a>Propiedades canónicas MAPI

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Una propiedad canónica es una propiedad virtual que representa una propiedad MAPI o varias propiedades MAPI definidas con el mismo identificador de propiedad. Las propiedades canónicas solo están diseñadas para facilitar la identificación coherente de las propiedades MAPI en discusiones o documentación fuera del código. A diferencia de los nombres de propiedades etiquetados definidos por MAPI, los nombres de propiedades canónicas no se definen como constantes globales en los archivos de encabezado MAPI.
  
## <a name="naming-conventions"></a>Convenciones de nomenclatura

Los nombres de propiedades canónicas comienzan con un prefijo, "Pid", que representa "identificador de propiedad". Según si la propiedad es una propiedad etiquetada, una propiedad con nombre con un identificador numérico o una propiedad con nombre con un nombre de cadena, el prefijo se califica como "PidTag", "PidLid" y "PidName", respectivamente. Por ejemplo, [PidTagAccount](pidtagaccount-canonical-property.md) representa las propiedades etiquetadas, **PR_ACCOUNT** ([PidTagAccount](pidtagaccount-canonical-property.md)), **PR_ACCOUNT_A** ([PidTagAccount](pidtagaccount-canonical-property.md)) y **PR_ACCOUNT_W** ([PidTagAccount](pidtagaccount-canonical-property.md)), que especifican el nombre de cuenta de un destinatario; [PidLidContacts](pidlidcontacts-canonical-property.md) representa la **propiedad dispidContacts,** una propiedad con nombre que tiene un identificador numérico y que especifica el nombre de los contactos asociados a un mensaje; y [PidNamePhishingStamp](pidnamephishingstamp-canonical-property.md) representa " ," una propiedad con nombre que tiene un nombre de cadena y que especifica los mensajes de marcado de cadena que probablemente sean http://schemas.microsoft.com/outlook/phishingstamp phishing. 
  
## <a name="representing-similar-properties-using-one-canonical-property"></a>Representar propiedades similares mediante una propiedad canónica

### <a name="identifying-properties-in-mapi"></a>Identificación de propiedades en MAPI

Todas las propiedades de MAPI se identifican mediante un identificador de propiedad que es un valor de 16 bits sin signo. El identificador de propiedad y el tipo de propiedad (otro valor de 16 bits sin signo) constituyen una etiqueta de propiedad para la propiedad. 
  
MAPI usa una etiqueta de propiedad para definir de forma única las propiedades. Las propiedades que tienen la misma etiqueta de propiedad, como **PR_BUSINESS2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)) y **PR_OFFICE2_TELEPHONE_NUMBER** ([PidTagBusiness2TelephoneNumber](pidtagbusiness2telephonenumber-canonical-property.md)), se consideran propiedades idénticas en MAPI. Para obtener una lista de etiquetas de propiedad que MAPI ha definido para sus propias propiedades, vea el archivo de encabezado MAPI, Mapitags.h.
  
Tenga en cuenta que MAPI divide los identificadores de propiedad en intervalos. Donde un identificador se encuentra en el intervalo indica su uso y propiedad. Los identificadores de propiedad de las propiedades etiquetadas están en el intervalo de 0x0001 a 0x7FFF. Dentro de este intervalo se encuentran los identificadores de propiedad de las propiedades definidas por MAPI, que se encuentran en el intervalo de 0x0001 a 0x3FFF. Los identificadores de propiedad de las propiedades con nombre están en el intervalo de 0x8000 a 0x8FFF. 
  
Las propiedades con nombre se atribuyen además mediante un conjunto de propiedades y un identificador largo (LID), que es un valor de 32 bits sin signo, o una cadena. Un conjunto de propiedades es un GUID que identifica un grupo de propiedades con nombre con un propósito similar. El conjunto de propiedades y el nombre de lid o cadena se usan para obtener o establecer la propiedad con nombre.
  
### <a name="property-type"></a>Tipo de propiedad

Aparte de los identificadores, un tipo de datos atribuyó una propiedad que especifica el tipo de valores permitidos para esa propiedad.
  
Para las propiedades del tipo de cadena, según la compatibilidad de Unicode en la plataforma subyacente, la propiedad puede ser de tipo PT_STRING8 (cadena de caracteres de 8 bits terminada en null) o PT_UNICODE (cadena Unicode terminada en null). Una propiedad se puede definir con el tipo PT_TSTRING y, según la configuración de compilación, PT_TSTRING tiene como valor predeterminado una cadena Unicode para plataformas compatibles con Unicode o una cadena PT_STRING8 para plataformas compatibles con ANSI o DBCS. Es común que una propiedad con tipo de cadena se identifique mediante tres nombres similares, como **PR_ACCOUNT**, **PR_ACCOUNT_A** y **PR_ACCOUNT_W**, que son del tipo PT_TSTRING, PT_STRING8 y PT_UNICODE respectivamente.
  
Para obtener más información sobre tipos de propiedades y macros relacionadas con tipos, vea el archivo de encabezado MAPI, Mapidefs.h.
  
### <a name="identifying-similar-properties"></a>Identificación de propiedades similares

En el panorama actual de propiedades MAPI, no es raro encontrar que una propiedad se ha expuesto bajo nombres de propiedad diferentes, todos los cuales se definen con el mismo identificador de propiedad. Por ejemplo, las propiedades etiquetadas, **PR_BUSINESS2_TELEPHONE_NUMBER** y **PR_OFFICE2_TELEPHONE_NUMBER**, se definen en Mapitags.h para tener el mismo identificador y tipo de propiedad. Estas dos propiedades están estrechamente relacionadas:
  
- **PR_BUSINESS2_TELEPHONE_NUMBER_A**
    
- **PR_BUSINESS2_TELEPHONE_NUMBER_W**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_A**
    
- **PR_OFFICE2_TELEPHONE_NUMBER_W**
    
Las propiedades con el sufijo "_A" se escriben como PT_STRING8 y las que tienen el sufijo "_W" se escriben como PT_UNICODE.
  
El propósito de una propiedad canónica, **PidTagBusiness2TelephoneNumber** en este ejemplo, es facilitar la referencia a estas propiedades MAPI estrechamente afiliadas mediante un identificador y de forma coherente (usando el prefijo "Pid") en todas las propiedades MAPI. Para buscar qué propiedades MAPI reales representa una propiedad canónica, vea [Mapping Canonical Property Names to MAPI Names](mapping-canonical-property-names-to-mapi-names.md). Para buscar la propiedad canónica a la que está asociada una propiedad MAPI, vea [Mapping MAPI Names to Canonical Property Names](mapping-mapi-names-to-canonical-property-names.md).
  
## <a name="mapi-support-of-canonical-property-names"></a>Compatibilidad con MAPI de nombres de propiedades canónicas

Dado que las propiedades canónicas no son propiedades reales y no se definen en archivos de encabezado MAPI, no debe usar nombres de propiedades canónicas en el código; en su lugar, debe seguir usando los nombres exactos de las propiedades MAPI en el código. Por ejemplo, puede  hacer referencia PR_BUSINESS2_TELEPHONE_NUMBER y **PR_OFFICE2_TELEPHONE_NUMBER** fuera del código como **PidTagBusiness2TelephoneNumber** y usar PR_BUSINESS2_TELEPHONE_NUMBER o **PR_OFFICE2_TELEPHONE_NUMBER** código.  
  
Si debe usar nombres de propiedades canónicas en el código, primero debe definirlos en sus propios archivos de encabezado.
  
## <a name="canonical-property-names-and-exchange-protocol-specifications"></a>Nombres de propiedades canónicas y Exchange de protocolo

Los nombres canónicos se hacen referencia Microsoft Exchange Server especificaciones de protocolo que Exchange Server para comunicarse con otros productos de Microsoft. Para obtener más información acerca de las propiedades del objeto de mensaje a las que se hace referencia Exchange especificaciones del protocolo, vea [[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx).
  
## <a name="see-also"></a>Vea también



[Etiquetas de propiedad MAPI](mapi-property-tags.md)
  
[Información general del identificador de propiedad MAPI](mapi-property-identifier-overview.md)
  
[Información general del tipo de propiedad MAPI](mapi-property-type-overview.md)

