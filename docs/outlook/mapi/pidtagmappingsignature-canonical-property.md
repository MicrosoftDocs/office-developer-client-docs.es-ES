---
title: Propiedad canónica PidTagMappingSignature
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342554"
---
# <a name="pidtagmappingsignature-canonical-property"></a>Propiedad canónica PidTagMappingSignature

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene la firma de asignación para las propiedades con nombre de un objeto MAPI determinado. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|Identificador:  <br/> |0x0FF8  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que los objetos con propiedades con nombre exponen esta propiedad. Una aplicación cliente debe comprobar la **PR_MAPPING_SIGNATURE** propiedad de ambos objetos al copiar propiedades con nombre de un objeto a otro. El uso de esta propiedad puede minimizar la traducción entre los nombres e identificadores de las propiedades copiadas. 
  
Si esta propiedad no existe para un objeto MAPI determinado, el objeto tiene su propia asignación única de nombres e identificadores. En este caso, el cliente debe llamar al método [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) en el objeto de origen y, a continuación, al método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) en el objeto de destino. 
  
Cuando dos objetos tienen el mismo **PR_MAPPING_SIGNATURE** valor, el cliente no necesita traducir el nombre al identificador y al nombre. El cliente simplemente puede llamar al método [IMAPIProp::GetProps](imapiprop-getprops.md) en el origen y, a continuación, al método [IMAPIProp::SetProps](imapiprop-setprops.md) en el destino. Esto es conveniente para los clientes que realizan copias personalizadas de propiedades con nombre y para los proveedores que implementan los métodos [IMAPIProp::CopyTo](imapiprop-copyto.md) e [IMAPIProp::CopyProps.](imapiprop-copyprops.md) 
  
Para obtener más información sobre las propiedades con nombre y la asignación de nombres e identificadores, vea [MAPI Named Properties](mapi-named-properties.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[MAPINAMEID](mapinameid.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

