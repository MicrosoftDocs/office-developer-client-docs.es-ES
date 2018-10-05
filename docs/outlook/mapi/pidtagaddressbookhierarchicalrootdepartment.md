---
title: Propiedad canónica PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382613"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>Propiedad canónica PidTagAddressBookHierarchicalRootDepartment

  
  
**Hace referencia a**: Outlook 2013 | Outlook 2016 
  
 Contiene el nombre distintivo (DN) de la raíz de direcciones jerárquicas (HAB). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|Conjunto de propiedades:  <br/> |Libreta de direcciones  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x8C98  <br/> |
|Tipo de datos:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Libreta de direcciones de Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Esto es una propiedad en el contenedor de (GAL) de la lista global de direcciones y representa el nombre distintivo (DN) de la raíz de direcciones jerárquica. Esta propiedad sólo está presente en la libreta de direcciones sin conexión y nunca en los servicios de dominio de Active Directory (AD DS). Los llamadores deben pasar MAPI_CACHE_ONLY a la llamada GetProps para evitar una llamada a procedimiento remoto. Si esto no está presente, los llamadores deben utilizar PR_EMS_AB_HAB_ROOT_DEPARTMENT, que es del tipo pt Object, para buscar el departamento de raíz. 
  
Una vez obtenido el departamento de raíz, puede tener un tipo de objeto MAPI_MAILUSER o MAPI_DISTLIST. Si el tipo de objeto es MAPI_DISTLIST, que se emplea el nuevo esquema. Si el tipo de objeto es MAPI_MAILUSER, que se emplea el esquema anterior. 
  
- Microsoft Office Outlook 2007 Service Pack 2 es compatible con ambos esquemas. 
    
- Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten el nuevo esquema.
    
En el esquema de nuevo, todos los grupos departamentales también son listas de distribución y son de tipo MAPI_DISTLIST. Los miembros de grupos departamentales y departamentos dentro de los grupos de departamentos se obtienen mediante PR_EMS_AB_MEMBER, exactamente igual que los miembros de lista de distribución.
  
Una vez obtenido el departamento de raíz, puede tener un tipo de objeto MAPI_MAILUSER o MAPI_DISTLIST. Si el tipo de objeto es MAPI_DISTLIST, se utiliza el esquema de nuevo. Si el tipo de objeto es MAPI_MAILUSER, se utiliza el esquema de la antiguo. 
  
En el esquema de nuevo, todos los grupos de departamentos también son listas de distribución y son de tipo MAPI_DISTLIST.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones de protocolo de Microsoft Exchange Server relacionadas.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

