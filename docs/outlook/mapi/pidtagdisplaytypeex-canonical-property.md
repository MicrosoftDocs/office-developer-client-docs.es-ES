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
ms.openlocfilehash: 30482f7d6acef7377a1b63bc3de4e43be48d8608
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583361"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>Propiedad canónica PidTagDisplayTypeEx

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene el tipo de una entrada, con respecto a cómo se debe mostrar la entrada de una fila en una tabla de la lista Global de direcciones. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Identificador:  <br/> |0x3905  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Libreta de direcciones MAPI  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad especifica el tipo de una entrada, con respecto a determinar cómo deben mostrarse en la lista Global de direcciones. Se proporciona información adicional que no se pueden representar en **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
  
> [!NOTE]
> Los valores de **PR_DISPLAY_TYPE** y esta propiedad comienzan con "DT_" y se definen en Mapitags.h. Todos los valores no documentados están reservados para MAPI. Las aplicaciones cliente no deben definir los nuevos valores y deben estar preparadas abordar los problemas con un valor sin documentar. 
  
Hay algunas macros que pueden ayudar a determinar los atributos de un objeto como si es local, remoto o con control de seguridad. Estas macros se incluyen: 
  
|**Macro**|**Valor**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0 x 80000000)  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0 x 40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID(v)  <br/> |(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE(v)  <br/> |(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE(v)  <br/> |(((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL(v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|POR EJEMPLO  <br/> |((ULONG) 0 X 00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0 X 00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0 X 00000009)  <br/> |
   
Las siguientes son algunas notas sobre cómo usar estas macros. 
  
- Para comprobar si una entrada es una entrada remota en otro bosque, se aplican la macro DTE_IS_REMOTE_VALID para el valor de esta propiedad para comprobar si se ha establecido el indicador DTE_FLAG_REMOTE_VALID en la entrada. Si es una entrada de remota, a continuación, puede encontrar el tipo de la entrada de remota mediante el uso de la macro DTE_REMOTE. 
    
- En las configuraciones de un solo bosque y entre bosques, cuando **PR_DISPLAY_TYPE** tiene el valor de DT_DISTLIST y DTE_IS_REMOTE_VALID es false, la aplicación de la macro DTE_LOCAL para el valor de esta propiedad puede dejar que aún más identificar el tipo del objeto como o bien DT_DISTLIST (una lista de distribución) o DT_SEC_DISTLIST (una lista de distribución de seguridad). 
    
- Si aplica la macro DTE_LOCAL para el valor de **PR_DISPLAY_TYPE_EX** y devuelve el tipo DT_REMOTE_MAILUSER, a continuación, el movimiento es un movimiento remoto. 
    
- En un solo bosque o en una configuración entre bosques donde replicación está controlada por una lista de Control de acceso (ACL), puede usar la macro DTE_IS_ACL_CAPABLE para determinar si una entrada es una entidad de seguridad.
    
En una configuración entre bosques, **PR_DISPLAY_TYPE** tiene el valor de DT_REMOTE_MAILUSER. Aplicar la macro DTE_REMOTE para el valor de esta propiedad puede dejar que obtener el tipo de la entrada remoto. Los posibles tipos de entrada remoto son los siguientes: 
  
|**Tipo de movimiento remoto**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0 X 00000003)  <br/> |Lista de distribución dinámica.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0 X 00000001)  <br/> |Lista de distribución.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0 X 00000008)  <br/> |Equipamiento, por ejemplo, una impresora o a proyectores.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0 X 00000000)  <br/> |Usuario con un buzón de correo.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0 X 00000000)  <br/> |Una entrada de la lista de direcciones en la lista Global de direcciones.  <br/> |
|POR EJEMPLO  <br/> |((ULONG) 0 X 00000007)  <br/> |Sala de conferencias.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0 X 00000009)  <br/> |Lista de distribución de seguridad.  <br/> |
   
En un solo bosque y en entre bosques configuración cuando **PR_DISPLAY_TYPE** tiene el valor de DT_DISTLIST y DTE_IS_REMOTE_VALID es false, la aplicación de la macro DTE_LOCAL para el valor de esta propiedad puede dejar que obtener el tipo de la lista de distribución . Los posibles tipos de lista de distribución son las siguientes: 
  
|**Tipo de lista de distribución**|**Valor**|**Descripción**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0 X 00000001)  <br/> |Lista de distribución.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0 X 00000009)  <br/> |Lista de distribución de seguridad.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de las propiedades que aparecen como nombres alternativos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

