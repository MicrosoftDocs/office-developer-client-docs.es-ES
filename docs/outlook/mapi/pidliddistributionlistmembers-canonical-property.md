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
ms.openlocfilehash: 9bfb94b2929f780a428fb932efb3538f94f5aaea
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591467"
---
# <a name="pidliddistributionlistmembers-canonical-property"></a>Propiedad canónica PidLidDistributionListMembers

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica la lista de identificadores de los objetos que corresponden a los miembros de la lista de distribución personal.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidDLMembers  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008055  <br/> |
|Tipo de datos:  <br/> |PT_MV_BINARY  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Los miembros de la lista de distribución personal pueden ser otras listas de distribución personales, las direcciones electrónicas contenidas en un contacto, los usuarios de la lista Global de direcciones o listas de distribución o direcciones de correo electrónico de uso único. El formato de cada propiedad EntryId debe ser un EntryId de uso único, tal como se especifica en [[MS-OXCDATA],](http://msdn.microsoft.com/library/1afa0cd9-b1a0-4520-b623-bf15030af5d8%28Office.15%29.aspx) o un valor de EntryId ajustado. 
  
Al establecer esta propiedad, el cliente o el servidor debe asegurarse de que su tamaño total es inferior a 15.000 bytes.
  
Esta propiedad especifica la lista de identificadores de uso único que corresponden a los miembros de la lista de distribución personal. Estos identificadores de uso único encapsulan para mostrar los nombres y direcciones de correo electrónico de los miembros de la lista de distribución personal.
  
Si el cliente o el servidor de establece esta propiedad, se debe sincronizar con esta propiedad **dispidDLMembers** para cada entrada en la propiedad **dispidDLOneOffMembers** ([PidLidDistributionListOneOffMembers](pidliddistributionlistoneoffmembers-canonical-property.md)), debe haber una entrada en el misma posición en el **dispidDLOneOffMembers**.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

