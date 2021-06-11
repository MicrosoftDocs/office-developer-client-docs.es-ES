---
title: Propiedad canónica PidLidDistributionListMembers
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidDistributionListMembers
api_type:
- COM
ms.assetid: 029767ab-de72-4402-9cc3-31b006591042
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f04d1593e2a13a2bfc23412340d7eb9f38f5d9ef
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335073"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>Propiedad canónica PidLidDistributionListMembers

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica la lista de EntryIds de los objetos que corresponden a los miembros de la lista de distribución personal.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidDLMembers  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Id. largo (LID):  <br/> |0x00008055  <br/> |
|Tipo de datos:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Los miembros de la lista de distribución personal pueden ser otras listas de distribución personales, direcciones electrónicas contenidas en un contacto, usuarios de lista global de direcciones o listas de distribución, o direcciones de correo electrónico únicas. El formato de cada EntryId debe ser un EntryId único, como se especifica en [[MS-OXCDATA],](https://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) o un EntryId ajustado. 
  
Al establecer esta propiedad, el cliente o el servidor deben asegurarse de que su tamaño total es inferior a 15 000 bytes.
  
Esta propiedad especifica la lista de entryids únicos que corresponden a los miembros de la lista de distribución personal. Estos EntryIds únicos encapsulan los nombres para mostrar y las direcciones de correo electrónico de los miembros de la lista de distribución personal.
  
Si el cliente o el servidor establecen esta propiedad, debe sincronizarse con esta propiedad **dispidDLMembers** para cada entrada de la propiedad **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), debe haber una entrada en la misma posición en **la dispidDLOneOffMembers**.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

