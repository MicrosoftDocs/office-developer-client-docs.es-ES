---
title: Propiedad canónica PidTagEmsAbServer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEmsAbServer
api_type:
- HeaderDef
ms.assetid: de942619-2507-8fe0-bc81-f9da9ef7266f
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fba49b052a51bd498f61fc115f630d08fc6c8926
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384983"
---
# <a name="pidtagemsabserver-canonical-property"></a>Propiedad canónica PidTagEmsAbServer

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
Especifica la ruta de acceso de un contenedor de la libreta de direcciones en un escenario sin conexión o el nombre de dominio completo del servidor de catálogo global donde reside el contenedor de la libreta de direcciones en un escenario en línea.
  
## 

|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EMS_AB_SERVER, PR_EMS_AB_SERVER_A, PR_EMS_AB_SERVER_W  <br/> |
|Identificador:  <br/> |0xFFFE  <br/> |
|Tipo de datos:  <br/> |PT_TSTRING  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad tiene el tipo de propiedad restablecer a **PT_UNICODE** cuando se compila con el `UNICODE` símbolo en una plataforma de Unicode y a **PT_STRING8** cuando no se compila con el `UNICODE` símbolo. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

