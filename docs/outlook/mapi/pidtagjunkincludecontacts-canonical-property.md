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
ms.openlocfilehash: 7e61e98d1db1ab3acb958da353d8d22870937632
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328717"
---
# <a name="pidtagjunkincludecontacts-canonical-property"></a>Propiedad canónica PidTagJunkIncludeContacts

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica si las direcciones de correo electrónico de los contactos de la carpeta Contactos se tratan especialmente con respecto al filtro de correo no deseado.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_JUNK_INCLUDE_CONTACTS  <br/> |
|Identificador:  <br/> |0x6100  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Correo no deseado  <br/> |
   
## <a name="remarks"></a>Comentarios

Si se establece en "0x00000001", estas direcciones de correo electrónico deben rellenar la parte de dirección de correo electrónico de contacto de "confianza" de la restricción de regla de correo electrónico no deseado de forma que el correo de estas direcciones se trate como "correo no deseado". Si se establece en "0x00000000", las direcciones de correo electrónico de la carpeta Contactos no deben agregarse a la regla de correo electrónico no deseado y la sección de la regla debe ser NULL.
  
Si esta propiedad está presente con un valor de "0x00000001" y el contacto agregado tiene direcciones de correo electrónico que aún no se incluyen en la sección de contactos de confianza de la regla de correo electrónico no deseado, dichas direcciones de correo electrónico deben agregarse a la restricción. Si esta propiedad es "0x00000000", no se requiere ninguna acción.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Permite el control de listas de permitidos o bloqueados y la determinación de mensajes de correo no deseado.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

