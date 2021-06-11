---
title: Propiedad canónica PidTagGeneration
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagGeneration
api_type:
- HeaderDef
ms.assetid: 81c2e479-84a1-42ba-a9ce-25e3fc8d80cb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f8a2c92e47c2f309cd52f80c0cb5cf5d1f3518e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316138"
---
# <a name="pidtaggeneration-canonical-property"></a>Propiedad canónica PidTagGeneration

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una abreviatura generacional que sigue el nombre completo del destinatario. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_GENERATION, PR_GENERATION_A, PR_GENERATION_W  <br/> |
|Identificador:  <br/> |0x3A05  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Usuario de correo MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Estas propiedades proporcionan información de identificación y acceso sobre un destinatario. El destinatario y su organización los definen. 
  
Los valores comunes incluyen Jr., Sr. y III.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones de listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

