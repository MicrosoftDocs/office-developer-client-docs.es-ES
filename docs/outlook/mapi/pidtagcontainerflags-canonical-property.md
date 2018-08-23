---
title: Propiedad canónica PidTagContainerFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: b62fc62bb9232b7106019fca82f502221e50bad0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583564"
---
# <a name="pidtagcontainerflags-canonical-property"></a>Propiedad canónica PidTagContainerFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de bits de indicadores que describen las capacidades de un contenedor de la libreta de direcciones. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Identificador:  <br/> |0x3600  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

La máscara de bits se pueden establecer uno o varios de los siguientes indicadores:
  
AB_FIND_ON_OPEN 
  
> Muestra un cuadro de diálogo para solicitar una restricción antes de mostrar cualquier contenido del contenedor. 
    
AB_MODIFIABLE 
  
> Las entradas se pueden agregar a y elimina del contenedor. Esta marca no indica si se pueden modificar las entradas en el contenedor.
    
AB_RECIPIENTS 
  
> Puede contener el contenedor destinatarios. Esta marca no indica si todos los destinatarios están realmente presentes en el contenedor o si se agreguen o se eliminen. 
    
AB_SUBCONTAINERS 
  
> El contenedor puede contener a secundarias contenedores. Esta marca no indicar si están realmente presentes en el contenedor de cualquier subcontenedores, ni si se agreguen o se eliminen. AB_SUBCONTAINERS se debe establecer para que el contenedor admitir [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md). 
    
AB_UNMODIFIABLE 
  
> Las entradas se no se pueden agregar o quitar del contenedor. Esta marca no indica si se pueden modificar las entradas en el contenedor. 
    
El indicador AB_FIND_ON_OPEN es muy recomendable para contenedores utilizados con los servicios en línea o con conexiones lentas a los servidores. Cuando se abre un contenedor que tiene AB_FIND_ON_OPEN establecido, se presenta un cuadro de diálogo **Buscar** para restringir los usuarios de mensajería que se muestra al usuario. Incluso una especificación parcial limitar los usuarios de mensajería puede acelerar considerablemente una presentación del contenido. 
  
Se debe establecer la marca de la AB_MODIFIABLE o AB_UNMODIFIABLE. Ambos indicadores se pueden establecer para indicar que el contenedor no sabe si se puede modificar o no, por ejemplo si modificación depende de los derechos de acceso del usuario. En este caso, una aplicación cliente debe intentar una llamada y examinar el código de retorno para determinar las capacidades del contenedor. Normalmente se inicia un cliente mediante el examen de AB_MODIFIABLE. Si se establece, el cliente realiza una llamada que intenta modificar el contenedor y comprueba el valor devuelto. 
  
El indicador AB_MODIFIABLE no indica qué tipos de entradas se pueden agregar al contenedor. Para determinar esto, el cliente debe usar el método [OpenProperty](imapiprop-openproperty.md) apropiado para abrir la propiedad del contenedor **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Apertura **PR_CREATE_TEMPLATES** causas de la tabla de uso único del contenedor que debe ser devuelto, los tipos de entradas que se pueden crear en el contenedor de lista. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones para las listas de los usuarios, contactos, grupos y recursos.
    
[[MS-NSPI]](http://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Administra las comunicaciones de un cliente con un servidor de la interfaz de proveedor de servicio de nombres (NSPI).
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene las definiciones de propiedades que se muestran como propiedades asociadas.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

