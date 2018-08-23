---
title: Propiedad canónica PidLidContactItemData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: f363b0a756a2cf4c7e37854cab0ddc4a46a0754d
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582661"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Propiedad canónica PidLidContactItemData

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se usa para mostrar la información de contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidContactItemData  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Identificador de tipo Long (LID):  <br/> |0x00008007  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Si está presente, la propiedad debe tener seis entradas, cada una correspondiente a un campo visible en la interfaz de usuario de la aplicación.
  
|**Índice basado en uno en la propiedad de varios valores**|**El valor debe ser uno de los siguientes**|**Descripción**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |La aplicación debe mostrar la dirección del contacto principal.  <br/> |
|1  <br/> |0 x 00000002 o 0 x 00000000  <br/> |La aplicación debe mostrar el trabajo del contacto.  <br/> |
|1  <br/> |0 x 00000003  <br/> |La aplicación debe mostrar el contacto de la otra dirección.  <br/> |
|2  <br/> |0x00008080  <br/> |La aplicación debe mostrar correo electrónico1.  <br/> |
|2  <br/> |0x00008090  <br/> |La aplicación debe mostrar correo electrónico 2.  <br/> |
|2  <br/> |0x000080A0  <br/> |La aplicación debe mostrar correo electrónico 3.  <br/> |
|3,4,5,6  <br/> |PropertyID de cualquiera de las propiedades de teléfono o cualquiera de los números de fax que se especifican en [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).  <br/> |La aplicación debe mostrar la propiedad correspondiente.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones de protocolo

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y las referencias a las especificaciones del protocolo de Exchange Server relacionadas.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y operaciones que se permiten para los contactos y las listas de distribución personal.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Recursos adicionales



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades MAPI canónicas](mapi-canonical-properties.md)
  
[Asignar nombres de propiedad canónicos a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignar nombres MAPI a los nombres de propiedad canónico](mapping-mapi-names-to-canonical-property-names.md)

