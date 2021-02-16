---
title: Propiedad canónica PidLidFlagRequest
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357809"
---
# <a name="pidlidflagrequest-canonical-property"></a>Propiedad canónica PidLidFlagRequest

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa el estado de una solicitud de reunión.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidRequest  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x00008530  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Marcar  <br/> |
   
## <a name="remarks"></a>Comentarios

En Microsoft Office Outlook, una solicitud de reunión es un elemento de cita.
  
Esta propiedad contiene texto que el usuario puede asociar a la marca y se debe establecer si el objeto de mensaje está marcado o completado, pero no debe existir para un objeto relacionado con la reunión. Los clientes pueden optar por no admitir esta propiedad y escribir siempre "Seguimiento" (traducido al idioma del usuario si corresponde) como el valor de la cadena cuando se debe establecer esta propiedad. Esta propiedad debe omitirse condicionalmente en función de los valores de las propiedades **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) y **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones relacionadas con la marcación.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

