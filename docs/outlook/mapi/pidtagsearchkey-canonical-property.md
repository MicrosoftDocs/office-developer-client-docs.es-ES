---
title: Propiedad canónica PidTagSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345468"
---
# <a name="pidtagsearchkey-canonical-property"></a>Propiedad canónica PidTagSearchKey

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una clave binaria comparable que identifica objetos correlacionados para una búsqueda.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x300B  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de id.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona un seguimiento de objetos relacionados, como copias de mensajes, y facilita la búsqueda de repeticiones no deseadas, como destinatarios duplicados.
  
MAPI usa reglas específicas para crear claves de búsqueda para destinatarios de mensajes. La clave de búsqueda se forma concatenando el tipo de dirección (en mayúsculas), el carácter de dos puntos ':', la dirección de correo electrónico en forma canónica y el carácter nulo de terminación. El formulario canónico aquí significa que las direcciones que distinguen mayúsculas de minúsculas aparecen en el caso correcto y las direcciones que no distinguen mayúsculas de minúsculas se convierten en mayúsculas. Esto es importante para conservar las correlaciones entre mensajes.
  
Para los objetos de mensaje, esta propiedad está disponible a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) inmediatamente después de la creación del mensaje. Para otros objetos, está disponible después de la primera llamada al método [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Dado que esta propiedad es modificable, no es confiable obtenerla a través de **GetProps** hasta que una llamada a **SaveChanges** haya confirmado los valores establecidos o modificados por el método [IMAPIProp::SetProps.](imapiprop-setprops.md) 
  
Para los perfiles, MAPI también proporciona una sección de perfil codificado de forma MUID_PROFILE_INSTANCE **,** con esta propiedad como su única propiedad. Se garantiza que esta clave es única entre todos los perfiles creados y puede ser más confiable que la propiedad **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), que puede, por ejemplo, eliminarse y volver a crearse con el mismo nombre.
  
En la tabla siguiente se resumen las diferencias importantes entre el PR_ENTRYID **(** [PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) y esta propiedad.
  
|**Característica**|PR_ENTRYID****|PR_RECORD_KEY****|PR_SEARCH_KEY****|
|:-----|:-----|:-----|:-----|
|Obligatorio en objetos de datos adjuntos  <br/> |No  <br/> |Sí  <br/> |No  <br/> |
|Obligatorio en objetos de carpeta  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Obligatorio en objetos de almacén de mensajes  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Obligatorio en objetos de estado  <br/> |Sí  <br/> |No  <br/> |No  <br/> |
|Creatable por cliente  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|Disponible antes **de SaveChanges** <br/> |Depende de la implementación del proveedor  <br/> |Depende de la implementación del proveedor  <br/> |En el caso de los mensajes, sí. Para otros, depende de la implementación del proveedor.  <br/> |
|Cambiado en una operación de copia  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Modificable por cliente después de una copia  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|Único dentro de ...  <br/> |Mundo entero  <br/> |Instancia de proveedor  <br/> |Mundo entero  <br/> |
|Binario comparable (como con memcmp)  <br/> |No: use [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Sí  <br/> |Sí  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedad canónica PidTagResponsibility](pidtagresponsibility-canonical-property.md)
  
[Propiedad canónica PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

