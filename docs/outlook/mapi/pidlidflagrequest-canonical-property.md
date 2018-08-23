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
ms.openlocfilehash: 4a2bcfbbc06427e5bf7e06f1c4060a29689fce3a
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22575395"
---
# <a name="pidlidflagrequest-canonical-property"></a>Propiedad canónica PidLidFlagRequest

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa el estado de una convocatoria de reunión.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidRequest  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Common  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008530  <br/> |
|Tipo de datos:  <br/> |PT_UNICODE  <br/> |
|Área:  <br/> |Marcar  <br/> |
   
## <a name="remarks"></a>Comentarios

En Microsoft Office Outlook, una convocatoria de reunión es un elemento de cita.
  
Esta propiedad contiene texto puede especificar el usuario que se asociará con la marca y se debería establecer, si el objeto de mensaje se marcan o completado, pero no debe existir para un objeto relacionado con la reunión. Los clientes pueden elegir no admite esta propiedad y escribir siempre "Seguimiento" (traducido para el idioma del usuario si es necesario) como el valor de la cadena cuando se debe establecer esta propiedad. Esta propiedad se debe omitir condicionalmente en función de los valores de las propiedades de **dispidValidFlagStringProof** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)) y **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones relacionadas con marcas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

