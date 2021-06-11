---
title: Propiedad canónica PidTagGender
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGender
api_type:
- HeaderDef
ms.assetid: a79a139a-6813-49f6-b622-bb66d62c4462
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b8ce3898ac021bc6eec2af6220889d71ff5a18dc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316159"
---
# <a name="pidtaggender-canonical-property"></a>Propiedad canónica PidTagGender

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el sexo del usuario de mensajería.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_GENDER  <br/> |
|Identificador:  <br/> |0x3A4D  <br/> |
|Tipo de datos:  <br/> |PT_I2  <br/> |
|Área:  <br/> |Usuario de correo MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad proporciona información de identificación y acceso sobre un usuario de mensajería y el contenido es. El contenido lo define el usuario de mensajería y la organización del usuario de mensajería. 
  
Los valores posibles para esta propiedad se definen en la enumeración de género. Se enumeran de la siguiente manera:
  
|**Enumeración de género**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|genderUnspecified  <br/> |0x0000  <br/> |El sexo del contacto no está especificado.  <br/> |
|genderFemale  <br/> |0x0001  <br/> |El contacto es mujer.  <br/> |
|genderMale  <br/> |0x0002  <br/> |El contacto es masculino.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.
    
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

