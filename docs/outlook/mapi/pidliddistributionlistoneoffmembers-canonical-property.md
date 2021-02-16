---
title: Propiedad canónica PidLidDistributionListOneOffMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListOneOffMembers
api_type:
- COM
ms.assetid: 0b92e654-9e2d-4c2e-9a63-d5fac603b0c0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fed4395274cb790ab8ab7ecf0456d4ecb9ec0134
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335052"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a>Propiedad canónica PidLidDistributionListOneOffMembers

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica la lista de EntryIds de uso único que corresponden a los miembros de la lista de distribución personal.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidDLOneOffMembers  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Long ID (LID):  <br/> |0x00008054  <br/> |
|Tipo de datos:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Estos EntryIds únicos encapsulan los nombres para mostrar y las direcciones de correo electrónico de los miembros de la lista de distribución personal.
  
Si el cliente o el servidor establecen esta propiedad, debe sincronizarse con la propiedad **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)): para cada entrada de la propiedad **dispidDLOneOffMembers,** debe haber una entrada en la misma posición en la propiedad **dispidDLMembers.** 
  
Al establecer **dispidDLOneOffMembers,** el cliente o el servidor debe asegurarse de que su tamaño total sea inferior a 15.000 bytes de tamaño.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

