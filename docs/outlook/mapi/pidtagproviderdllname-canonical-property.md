---
title: Propiedad canónica PidTagProviderDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagProviderDllName
api_type:
- COM
ms.assetid: 9ddb38eb-9a32-4dbe-b42c-6ea9db98acd2
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 57fdc754ed4be29dbdd50a198707d8f39a14b3d4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32286491"
---
# <a name="pidtagproviderdllname-canonical-property"></a>Propiedad canónica PidTagProviderDllName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de archivo base de la biblioteca de vínculos dinámicos (DLL) del proveedor de servicios MAPI.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_PROVIDER_DLL_NAME, PR_PROVIDER_DLL_NAME_A, PR_PROVIDER_DLL_NAME_W  <br/> |
|Identificador:  <br/> |0x300A  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Mapi común  <br/> |
   
## <a name="remarks"></a>Comentarios

MAPI usa una convención de nomenclatura de archivos DLL. Anexa la cadena 32 al nombre de dll base para identificar la versión que se ejecuta en plataformas de 32 bits. Por ejemplo, cuando se especifica el nombre MAPI.DLL, MAPI construye el nombre MAPI32.DLL para representar la versión de 32 bits correspondiente de la DLL.
  
Estas propiedades deben especificar el nombre base. MAPI anexa la cadena 32 según corresponda. La inclusión de la cadena 32 como parte de esta propiedad produce un error.
  
## <a name="related-resources"></a>Recursos relacionados

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

