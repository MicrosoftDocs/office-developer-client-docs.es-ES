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
ms.openlocfilehash: 54a0f438dacc8a1c7838eb538ec05c5c263f1b0a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32329277"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>Propiedad canónica PidTagNormalizedSubject

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el asunto del mensaje con cualquier prefijo quitado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Identificador:  <br/> |0x0E1D  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Correo electrónico  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades se calculan mediante el almacén de mensajes o los proveedores de transporte de las propiedades **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) y **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) de la siguiente manera.
  
- Si el **PR_SUBJECT_PREFIX** está presente y es una subcadena inicial de **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** y las propiedades asociadas se establecen en el contenido de **PR_SUBJECT** con el prefijo quitado. 
    
- Si **PR_SUBJECT_PREFIX** está presente, pero no es una subcadena inicial de **PR_SUBJECT**, **PR_SUBJECT_PREFIX** se elimina y vuelve a calcular de **PR_SUBJECT** mediante la siguiente regla: si la cadena contenida en **PR_SUBJECT** comienza con uno o tres caracteres no numéricos seguidos de dos puntos y un espacio, la cadena junto con los dos puntos y el espacio en blanco se convierte en el prefijo. Los números, los espacios en blanco y los caracteres de puntuación no son caracteres de prefijo válidos. 
    
- Si **PR_SUBJECT_PREFIX** no está presente, se calcula a partir **de PR_SUBJECT** la regla descrita en el paso anterior. A continuación, esta propiedad se establece en el contenido **de PR_SUBJECT** con el prefijo quitado. 
    
 **Nota** Cuando **PR_SUBJECT_PREFIX** es una cadena vacía, **PR_SUBJECT** y esta propiedad son las mismas. 
  
En última instancia, esta propiedad debe ser la parte de **PR_SUBJECT** siguiendo el prefijo. Si no hay ningún prefijo, esta propiedad se convierte en la misma que **PR_SUBJECT**.
  
 **PR_SUBJECT_PREFIX** y esta propiedad deben calcularse como parte de la [implementación de IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Una aplicación cliente no debe solicitar al método [IMAPIProp::GetProps](imapiprop-getprops.md) sus valores hasta que una llamada **IMAPIProp::SaveChanges** los haya confirmado. 
  
Las propiedades del asunto suelen ser pequeñas cadenas de menos de 256 caracteres y un proveedor de almacén de mensajes no está obligado a admitir la interfaz **IStream** de vinculación e inserción de objetos (OLE) en ellas. El cliente siempre debe intentar el acceso a través de la interfaz **IMAPIProp** primero y recurrir a **IStream** solo si MAPI_E_NOT_ENOUGH_MEMORY se devuelve. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

