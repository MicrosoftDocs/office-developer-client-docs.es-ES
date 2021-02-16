---
title: Propiedad canónica PidTagServiceDllName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagServiceDllName
api_type:
- COM
ms.assetid: a651af84-1711-449e-ba7e-5ce09cafa02b
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: adf24bcd02d7efc303f911ee01a64325150339ce
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32330068"
---
# <a name="pidtagservicedllname-canonical-property"></a>Propiedad canónica PidTagServiceDllName

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el nombre de archivo de la DLL que contiene la función de punto de entrada del proveedor de servicios de mensajes para llamar a la configuración.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_SERVICE_DLL_NAME, PR_SERVICE_DLL_NAME_A, PR_SERVICE_DLL_NAME_W  <br/> |
|Identificador:  <br/> |0x3D0A  <br/> |
|Tipo de datos:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Área:  <br/> |Perfil MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Cuando el nombre de la función de punto de entrada aparece en el **método PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md)), indica que el punto de entrada existe.
  
MAPI usa una convención de nomenclatura de archivos DLL. Anexa la cadena 32 al nombre de dll base para identificar la versión que se ejecuta en plataformas de 32 bits. Por ejemplo, cuando se especifica el nombre MAPI.DLL, MAPI construye el nombre MAPI32.DLL para representar la versión de 32 bits correspondiente de la DLL.
  
Estas propiedades deben especificar el nombre base. MAPI anexa la cadena 32 según corresponda. La inclusión de la cadena 32 como parte de estas propiedades produce un error.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Consulte también



[Propiedad canónica PidTagProviderDllName](pidtagproviderdllname-canonical-property.md)


[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

