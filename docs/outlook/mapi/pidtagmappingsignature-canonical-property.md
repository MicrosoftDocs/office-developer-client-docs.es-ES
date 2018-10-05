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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25396228"
---
# <a name="pidtagmappingsignature-canonical-property"></a>Propiedad canónica PidTagMappingSignature

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Contiene la firma de asignación para propiedades con nombre de un determinado objeto MAPI. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|Identificador:  <br/> |0x0FF8  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

Se recomienda que objetos tener propiedades con nombre exponen esta propiedad. Una aplicación cliente debe comprobar la propiedad **PR_MAPPING_SIGNATURE** de ambos objetos al copiar las propiedades de un objeto a otro con nombre. Uso de esta propiedad puede minimizar la traducción entre nombres e identificadores de las propiedades copiadas. 
  
Si esta propiedad no existe para un determinado objeto MAPI, a continuación, el objeto tiene su propia asignación de nombres y los identificadores único. En este caso el cliente debe llamar al método [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) en el objeto de origen y, a continuación, el método [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) en el objeto de destino. 
  
Cuando dos objetos tienen el mismo valor **PR_MAPPING_SIGNATURE** , el cliente no necesita traducir el nombre de identificador y el identificador para el nombre. El cliente puede llamar simplemente al método [IMAPIProp::GetProps](imapiprop-getprops.md) en el origen y, a continuación, el método [IMAPIProp::SetProps](imapiprop-setprops.md) en el destino. Esto es conveniente para los clientes que realizan copiar personalizado de propiedades con nombre y para los proveedores que implementan los métodos [IMAPIProp::CopyTo](imapiprop-copyto.md) y [IMAPIProp::CopyProps](imapiprop-copyprops.md) . 
  
Para obtener más información sobre las propiedades con nombre y la asignación de nombres y los identificadores, consulte [Propiedades de nombre de MAPI](mapi-named-properties.md). 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[MAPINAMEID](mapinameid.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

