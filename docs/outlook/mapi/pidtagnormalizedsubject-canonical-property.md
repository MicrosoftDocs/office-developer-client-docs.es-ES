---
title: Propiedad canónica PidTagNormalizedSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 74061f33a88dceb371cad00ef44f611b583f7ae2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/11/2018
ms.locfileid: "19819780"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>Propiedad canónica PidTagNormalizedSubject

  
  
**Hace referencia a**: Outlook 
  
Contiene al asunto del mensaje con cualquier prefijo que se ha quitado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Identificador:  <br/> |0x0E1D  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades se calculan por almacén de mensajes o los proveedores de las propiedades de **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) y **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) de transporte de la manera siguiente.
  
- Si el **PR_SUBJECT_PREFIX** está presente y es una subcadena inicial de **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** y las propiedades asociadas se establecen en el contenido de **PR_SUBJECT** con el prefijo que se ha quitado. 
    
- Si **PR_SUBJECT_PREFIX** está presente, pero no es una subcadena inicial de **PR_SUBJECT**, **PR_SUBJECT_PREFIX** se elimina y se vuelve a calcular desde **PR_SUBJECT** utilizando la siguiente regla: si la cadena contenida en **PR_SUBJECT** se comienza con uno a tres caracteres no numéricos, seguidos de un punto y coma y un espacio, a continuación, la cadena junto con los dos puntos y el espacio en blanco se convierte en el prefijo. Caracteres de números, espacios y signos de puntuación no son caracteres de prefijo válido. 
    
- Si **PR_SUBJECT_PREFIX** no está presente, se calcula a partir **PR_SUBJECT** utilizando la regla que se describen en el paso anterior. Esta propiedad, a continuación, se establece en el contenido de **PR_SUBJECT** con el prefijo que se ha quitado. 
    
 **Nota** Cuando **PR_SUBJECT_PREFIX** es una cadena vacía, **PR_SUBJECT** y esta propiedad son los mismos. 
  
En última instancia, esta propiedad debe ser la parte de **PR_SUBJECT** siguiendo el prefijo. Si no hay ningún prefijo, esta propiedad se convierte en el mismo como **PR_SUBJECT**.
  
 **PR_SUBJECT_PREFIX** y esta propiedad se deben calcular como parte de la implementación de [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Una aplicación de cliente no debe solicitar el método [IMAPIProp::GetProps](imapiprop-getprops.md) para sus valores hasta que se hayan confirmado por una llamada **IMAPIProp::SaveChanges** . 
  
Las propiedades de asunto son cadenas normalmente pequeñas de menos de 256 caracteres, y un proveedor de almacén de mensajes no está obligado a compatible con la interfaz de vinculación e incrustación de objetos (OLE) **IStream** en ellos. El cliente siempre debe intentar el acceso a través de la interfaz de **IMAPIProp** en primer lugar y recurrir a **IStream** sólo si se devuelve MAPI_E_NOT_ENOUGH_MEMORY. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla los objetos de mensaje y los datos adjuntos.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

