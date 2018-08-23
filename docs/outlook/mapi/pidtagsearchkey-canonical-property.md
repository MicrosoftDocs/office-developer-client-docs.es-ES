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
ms.openlocfilehash: da7d19407856570a628529877252360d1537bae7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22595394"
---
# <a name="pidtagsearchkey-canonical-property"></a>Propiedad canónica PidTagSearchKey

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una clave binario comparable que identifica objetos correlacionados para una búsqueda.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SEARCH_KEY  <br/> |
|Identificador:  <br/> |0x300B  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Propiedades de Id.  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona un seguimiento de los objetos relacionados, como copias de los mensajes y facilita encontrar repeticiones no deseadas, como destinatarios duplicados.
  
MAPI utiliza reglas específicas para la construcción de las claves de búsqueda para los destinatarios del mensaje. La clave de búsqueda se forma concatenando el tipo de dirección (en caracteres en mayúsculas), el carácter de punto y coma ':', la dirección de correo electrónico en forma canónica y el carácter nulo. Aquí forma canónica significa que distingue mayúsculas de minúsculas direcciones aparecen en mayúsculas y minúsculas, y las direcciones que no distinguen mayúsculas de minúsculas se convierten en mayúsculas. Esto es importante para preservar la correlación entre los mensajes.
  
Para los objetos de mensaje, esta propiedad está disponible a través del método [IMAPIProp::GetProps](imapiprop-getprops.md) inmediatamente después de la creación del mensaje. Para otros objetos, está disponible después de la primera llamada al método [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Debido a que esta propiedad es modificable, es poco confiable para obtenerlo a través de **GetProps** hasta que una llamada de **SaveChanges** haya confirmado cualquiera de los valores establecer o modificados por el método [IMAPIProp::SetProps](imapiprop-setprops.md) . 
  
Para los perfiles, MAPI también proporciona una sección de perfil codificado de forma rígida denominada **MUID_PROFILE_INSTANCE**, con esta propiedad como su propiedad único. Esta clave se garantiza que es único entre todos los perfiles que nunca se ha creado y puede ser más confiable que la propiedad **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), que puede, por ejemplo, eliminar y volver a crear con el mismo nombre.
  
En la siguiente tabla se resume las diferencias importantes entre la **entrada del objeto** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) y esta propiedad.
  
|**Característica**|ENTRADA DEL OBJETO ***|PR_RECORD_KEY ***|PR_SEARCH_KEY ***|
|:-----|:-----|:-----|:-----|
|Requerido en los objetos de datos adjuntos  <br/> |No  <br/> |Sí  <br/> |No  <br/> |
|Requerido en los objetos de carpeta  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Necesarios en los objetos de almacén de mensajes  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Requerido en los objetos de estado  <br/> |Sí  <br/> |No  <br/> |No  <br/> |
|Se puede crear por cliente  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|Disponible antes de **SaveChanges** <br/> |Depende de la implementación del proveedor  <br/> |Depende de la implementación del proveedor  <br/> |Para los mensajes, sí. Para otras personas, depende de la implementación del proveedor.  <br/> |
|Cambiado en una operación de copia  <br/> |Sí  <br/> |Sí  <br/> |No  <br/> |
|Se pueden cambiar después de una copia de los clientes  <br/> |No  <br/> |No  <br/> |Sí  <br/> |
|UNIQUE dentro de...  <br/> |Todo mundo  <br/> |Instancia de proveedor  <br/> |Todo mundo  <br/> |
|Binario comparable (como sucede con memcmp)  <br/> |No--usar [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Sí  <br/> |Sí  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedad canónica PidTagResponsibility](pidtagresponsibility-canonical-property.md)
  
[Propiedad canónica PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

