---
title: Propiedad canónica PidTagDisplayTypeEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6eea30188543cb06545a9efad705f5593d4227a7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360777"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>Propiedad canónica PidTagDisplayTypeEx

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el tipo de una entrada, con respecto a cómo debe mostrarse la entrada en una fila de una tabla para la lista global de direcciones. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Identificador:  <br/> |0x3905  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Libreta de direcciones MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica el tipo de una entrada, con respecto a cómo debe mostrarse en la lista global de direcciones. Proporciona información adicional que no puede representarse en **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
  
> [!NOTE]
> Los valores de tanto **PR_DISPLAY_TYPE** como esta propiedad comienzan por "DT_" y se definen en Mapitags. h. Todos los valores no documentados están reservados para MAPI. Las aplicaciones cliente no deben definir nuevos valores y deben estar preparadas para tratar con un valor no documentado. 
  
Hay algunas macros que pueden ayudar a determinar los atributos de un objeto, por ejemplo, si es local, remoto o controlado por seguridad. Entre estas macros se incluyen: 
  
|**Macro**|**Value**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID (v)  <br/> |(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE (v)  <br/> |(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE (v)  <br/> |(((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL (v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |
   
A continuación, se incluyen algunas notas sobre cómo usar estas macros. 
  
- Para comprobar si una entrada es una entrada remota en otro bosque, aplique la macro DTE_IS_REMOTE_VALID al valor de esta propiedad para comprobar si la marca DTE_FLAG_REMOTE_VALID está configurada en la entrada. Si se trata de una entrada remota, puede averiguar el tipo de la entrada remota mediante la macro DTE_REMOTE. 
    
- En las configuraciones de bosque único y entre bosques, cuando **PR_DISPLAY_TYPE** tiene el valor de DT_DISTLIST y DTE_IS_REMOTE_VALID es false, la aplicación de la macro DTE_LOCAL al valor de esta propiedad puede permitirle identificar aún más el tipo de objeto como ya sea DT_DISTLIST (una lista de distribución) o DT_SEC_DISTLIST (una lista de distribución de seguridad). 
    
- Si aplica la macro DTE_LOCAL al valor de **PR_DISPLAY_TYPE_EX** y devuelve el tipo DT_REMOTE_MAILUSER, la entrada es una entrada remota. 
    
- En un único bosque o en una configuración entre bosques donde la replicación está controlada por una lista de control de acceso (ACL), puede usar la macro DTE_IS_ACL_CAPABLE para determinar si una entrada es una entidad de seguridad.
    
En una configuración entre bosques, **PR_DISPLAY_TYPE** tiene el valor de DT_REMOTE_MAILUSER. Aplicar la macro DTE_REMOTE al valor de esta propiedad puede permitirle obtener el tipo de la entrada remota. Los tipos posibles de entrada remota son los siguientes: 
  
|**Tipo de entrada remota**|**Value**|**Descripción**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0x00000003)  <br/> |Lista de distribución dinámica.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |Lista de distribución.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |Equipo, por ejemplo, una impresora o un proyector.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Usuario con un buzón de correo.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Una entrada de la lista de direcciones en la lista global de direcciones.  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |Sala de conferencias.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Lista de distribución de seguridad.  <br/> |
   
En un solo bosque y en una configuración entre bosques, cuando **PR_DISPLAY_TYPE** tiene el valor de DT_DISTLIST y DTE_IS_REMOTE_VALID es false, la aplicación de la macro DTE_LOCAL al valor de esta propiedad puede permitirle obtener el tipo de la lista de distribución. . Los tipos de lista de distribución posibles son los siguientes: 
  
|**Tipo de lista de distribución**|**Value**|**Descripción**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |Lista de distribución.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Lista de distribución de seguridad.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

