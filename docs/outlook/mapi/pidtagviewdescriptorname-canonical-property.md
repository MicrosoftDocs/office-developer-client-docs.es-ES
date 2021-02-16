---
title: Propiedad canónica PidTagViewDescriptorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: ab906d83ae4ad46747fd9037728620db1d656d25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360728"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a>Propiedad canónica PidTagViewDescriptorName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de un descriptor de vista.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W  <br/> |
|Identificador:  <br/> |0x7006  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Transmitible definido por clase de mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades deben establecerse en una cadena no vacía para un mensaje de información de asociación de carpetas (FAI) que contenga definiciones de vista.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OCFGCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Especifica la ubicación y las propiedades de los datos de configuración de cliente y servidor, como listas de categorías compartidas y horas laborables.
    
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

