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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25383348"
---
# <a name="pidliddistributionlistoneoffmembers-canonical-property"></a>Propiedad canónica PidLidDistributionListOneOffMembers

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica la lista de identificadores de uso único que corresponden a los miembros de la lista de distribución personal.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidDLOneOffMembers  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008054  <br/> |
|Tipo de datos:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Estos identificadores de uso único encapsulan para mostrar los nombres y direcciones de correo electrónico de los miembros de la lista de distribución personal.
  
Si el cliente o el servidor establece esta propiedad, se debe sincronizar con la propiedad **dispidDLMembers** ([PidLidDistributionListMembers](pidliddistributionlistmembers-canonical-property.md)): para cada entrada en la propiedad **dispidDLOneOffMembers** , debe haber una entrada en la misma posición en la propiedad **dispidDLMembers** . 
  
Al establecer **dispidDLOneOffMembers**, el cliente o el servidor debe asegurarse de que su tamaño total es menor de tamaño 15.000 bytes.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

