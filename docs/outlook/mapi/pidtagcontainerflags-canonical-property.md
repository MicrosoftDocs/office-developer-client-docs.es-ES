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
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357550"
---
# <a name="pidtagcontainerflags-canonical-property"></a>Propiedad canónica PidTagContainerFlags

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene una máscara de direcciones de marcas que describen las capacidades de un contenedor de libreta de direcciones. 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Identificador:  <br/> |0x3600  <br/> |
|Tipo de datos:  <br/> |PT_LONG  <br/> |
|Área:  <br/> |Libreta de direcciones  <br/> |
   
## <a name="remarks"></a>Comentarios

Se pueden establecer uno o varios de los siguientes indicadores para la máscara de la máscara:
  
AB_FIND_ON_OPEN 
  
> Muestra un cuadro de diálogo para solicitar una restricción antes de mostrar el contenido del contenedor. 
    
AB_MODIFIABLE 
  
> Las entradas se pueden agregar y quitar del contenedor. Esta marca no indica si se pueden modificar las entradas del contenedor.
    
AB_RECIPIENTS 
  
> El contenedor puede contener a los destinatarios. Esta marca no indica si los destinatarios están realmente presentes en el contenedor o si se pueden agregar o quitar. 
    
AB_SUBCONTAINERS 
  
> El contenedor puede contener contenedores secundarios. Esta marca no indica si algún subcontenedor está realmente presente en el contenedor o si se pueden agregar o quitar. AB_SUBCONTAINERS debe establecerse para que el contenedor admita [IMAPIContainer:: GetHierarchyTable](imapicontainer-gethierarchytable.md). 
    
AB_UNMODIFIABLE 
  
> Las entradas no se pueden agregar ni quitar del contenedor. Esta marca no indica si se pueden modificar las entradas del contenedor. 
    
La marca AB_FIND_ON_OPEN es muy recomendable para los contenedores que se usan con servicios en línea o con conexiones lentas a los servidores. Cuando se abre un contenedor que tiene AB_FIND_ON_OPEN establecido, se presenta al usuario un cuadro de diálogo de **búsqueda** para restringir los usuarios de mensajería que se muestran. Incluso una especificación parcial que limita a los usuarios de mensajería puede acelerar drásticamente la presentación del contenido. 
  
Se debe establecer la marca AB_MODIFIABLE o AB_UNMODIFIABLE. Se pueden establecer ambas marcas para indicar que el contenedor no sabe si se puede modificar o no, por ejemplo, si la modificación depende de los derechos de acceso del usuario. En este caso, una aplicación cliente debe intentar una llamada y examinar el código de retorno para determinar las capacidades del contenedor. Un cliente suele empezar por examinar AB_MODIFIABLE. Si se establece, el cliente realiza una llamada que intenta modificar el contenedor y comprueba el valor devuelto. 
  
La marca AB_MODIFIABLE no indica los tipos de entradas que se pueden agregar al contenedor. Para determinarlo, el cliente debe usar el método [OpenProperty](imapiprop-openproperty.md) adecuado para abrir la propiedad **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) del contenedor. Al abrir **PR_CREATE_TEMPLATES** , se devuelve la tabla única del contenedor, que enumera los tipos de entradas que se pueden crear en el contenedor. 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona referencias a especificaciones del Protocolo de Exchange Server relacionadas.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones de las listas de usuarios, contactos, grupos y recursos.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Controla las comunicaciones de un cliente con un servidor de interfaz del proveedor de servicios de nombres (NSPI).
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs. h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags. h
  
> Contiene definiciones de propiedades que se enumeran como propiedades asociadas.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas de MAPI](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónica a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

