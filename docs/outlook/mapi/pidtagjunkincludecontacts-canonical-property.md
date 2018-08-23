---
title: Propiedad canónica PidTagJunkIncludeContacts
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagJunkIncludeContacts
api_type:
- HeaderDef
ms.assetid: 25368f6c-4fba-4381-840c-ca122bd31b5f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 121bba82a9ccd40a435769b5eb2d966ed60575f2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586973"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>Propiedad canónica PidTagJunkIncludeContacts

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si las direcciones de correo electrónico de los contactos de la carpeta Contactos se tratan especialmente en relación con el filtro de spam.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Identificador:  <br/> |0x6100  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Spam  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se establece en "0 x 00000001", estas direcciones de correo electrónico deben rellenar la parte de la dirección de correo electrónico de contacto "de confianza" de la restricción de regla de correo electrónico no deseado tal que el correo de estas direcciones se trata como "no deseado". Si se establece en "0 x 00000000", direcciones de correo electrónico desde la carpeta Contactos no deben ser agregadas a la regla de correo electrónico no deseado y la sección de la regla debe ser NULL.
  
Si esta propiedad está presente con un valor de "0 x 00000001" y si se ha agregado un contacto tiene direcciones de correo electrónico que no se han incluido en la sección de contactos de confianza de la regla de correo electrónico no deseado, esas direcciones de correo electrónico deben agregarse a la restricción. Si esta propiedad es "0 x 00000000", se requiere ninguna acción.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite la manipulación de las listas Permitir o bloquear y la determinación de los mensajes de correo electrónico no deseado.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

