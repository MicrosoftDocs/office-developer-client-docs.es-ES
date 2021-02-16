---
title: Propiedad canónica PidLidTaskActualEffort
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskActualEffort
api_type:
- COM
ms.assetid: 8e9a9432-bf50-4333-82ec-fba19dff8006
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 7eb51396f4575a8f8f9ce15aff84eb894773e979
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331174"
---
# <a name="pidlidtaskactualeffort-canonical-property"></a>Propiedad canónica PidLidTaskActualEffort

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Indica el número de minutos que el usuario realizó una tarea.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidTaskActualEffort  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008110  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Comentarios

El valor debe ser mayor o igual que 0 y menor que 0x5AE980DF (1.525.252.319), donde 480 minutos equivalen a un día y 2400 minutos a una semana (ocho horas en un día laborable y cinco días en una semana laboral).
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OJOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones permitidas para los objetos de lista de distribución personal y de contacto.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Consulte también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

