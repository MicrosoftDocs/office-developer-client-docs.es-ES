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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326127"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>Propiedad canónica PidTagAddressBookHierarchicalRootDepartment

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
 Contiene el nombre distintivo (DN) de la raíz jerárquica de direcciones (HAB). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|Conjunto de propiedades:  <br/> |Libreta de direcciones  <br/> |
|Id. largo (LID):  <br/> |0x8C98  <br/> |
|Tipo de datos:  <br/> |PT_STRING8  <br/> |
|Área:  <br/> |Libreta de direcciones de Exchange  <br/> |
   
## <a name="remarks"></a>Comentarios

Se trata de una propiedad en el contenedor de la lista global de direcciones (GAL) y representa el nombre distintivo de la raíz jerárquica de la dirección. Esta propiedad solo está presente en la libreta de direcciones sin conexión y nunca en Servicios de dominio de Active Directory (AD DS). Los autores de llamadas deben MAPI_CACHE_ONLY a la llamada GetProps para evitar una llamada de procedimiento remoto. Si no está presente, los autores de llamadas deben usar PR_EMS_AB_HAB_ROOT_DEPARTMENT, que es de tipo PT_OBJECT, para encontrar el departamento raíz. 
  
Una vez obtenido el departamento raíz, puede tener un tipo de objeto MAPI_MAILUSER o MAPI_DISTLIST. Si el tipo de objeto MAPI_DISTLIST, se está empleando el nuevo esquema. Si el tipo de objeto MAPI_MAILUSER, se está empleando el esquema anterior. 
  
- Microsoft Office Outlook 2007 Service Pack 2 admite ambos esquemas. 
    
- Microsoft Outlook 2010 y Microsoft Outlook 2013 admiten el nuevo esquema.
    
En el nuevo esquema, todos los grupos departamentales también son listas de distribución y son de tipo MAPI_DISTLIST. Los miembros de grupos departamentales y departamentos dentro de grupos departamentales se obtienen mediante el PR_EMS_AB_MEMBER, exactamente igual que los miembros de la lista de distribución.
  
Una vez obtenido el departamento raíz, puede tener un tipo de objeto MAPI_MAILUSER o MAPI_DISTLIST. Si el tipo de objeto MAPI_DISTLIST, se usa el nuevo esquema. Si el tipo de objeto MAPI_MAILUSER, se usa el esquema antiguo. 
  
En el nuevo esquema, todos los grupos departamentales también son DLs y son de tipo MAPI_DISTLIST.
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Microsoft Exchange Server protocolo relacionados.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

