---
title: Propiedad canónica PidTagAgingPeriod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAgingPeriod
api_type:
- HeaderDef
ms.assetid: 762020d1-4bc8-d60d-0f66-3929aae24bfb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: d42b58bf4fd445f34064b179c873c8bc15b11b3f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360119"
---
# <a name="pidtagagingperiod-canonical-property"></a>Propiedad canónica PidTagAgingPeriod

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Representa el número de unidades de tiempo que se usan para determinar el tiempo que un elemento permanece en una carpeta antes de que se archive el elemento.
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_AGING_PERIOD  <br/> |
|Identificador:  <br/> |0x36EC  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Varios  <br/> |
   
## <a name="remarks"></a>Comentarios

El tiempo que un elemento permanece en una carpeta antes de que se archive el elemento está determinado por dos propiedades, **PR_AGING_PERIOD** y **[PR_AGING_GRANULARITY](pidtagaginggranularity-canonical-property.md)**. **PR_AGING_GRANULARITY** representa la unidad de tiempo en **la que se PR_AGING_PERIOD,** al determinar este período de tiempo. 
  
Los valores posibles **para PR_AGING_GRANULARITY** pueden ser uno de los siguientes. 
  
****

|**Nombre**|**Descripción**|
|:-----|:-----|
|**AG_MONTHS** <br/> |**PR_AGING_PERIOD** se define en número de meses.  <br/> |
|**AG_WEEKS** <br/> |**PR_AGING_PERIOD** se define en número de semanas.  <br/> |
|**AG_DAYS** <br/> |**PR_AGING_PERIOD** se define en número de días.  <br/> |
   
Por ejemplo, si una carpeta archiva un elemento solo después de que el elemento haya estado en la carpeta durante dos semanas, **PR_AGING_GRANULARITY** es **AG_WEEKS** y **PR_AGING_PERIOD** es 2. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Define las estructuras de datos básicas que se usan en operaciones remotas.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los objetos de mensaje de correo electrónico.
    
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

