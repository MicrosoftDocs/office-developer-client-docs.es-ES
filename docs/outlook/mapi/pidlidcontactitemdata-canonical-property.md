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
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319513"
---
# <a name="pidlidcontactitemdata-canonical-property"></a>Propiedad canónica PidLidContactItemData

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Se usa para mostrar la información de contacto.
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |dispidContactItemData  <br/> |
|Conjunto de propiedades:  <br/> |PSETID_Address  <br/> |
|Id. largo (LID):  <br/> |0x00008007  <br/> |
|Tipo de datos:  <br/> |PT_MV_LONG  <br/> |
|Área:  <br/> |Contacto  <br/> |
   
## <a name="remarks"></a>Comentarios

Si está presente, la propiedad debe tener seis entradas, cada una correspondiente a un campo visible en la interfaz de usuario de la aplicación.
  
|**Índice basado en uno en la propiedad multivalor**|**El valor debe ser uno de los siguientes**|**Descripción**|
|:-----|:-----|:-----|
|1  <br/> |0x00000001  <br/> |La aplicación debe mostrar la dirección principal del contacto.  <br/> |
|1  <br/> |0x00000002 o 0x00000000  <br/> |La aplicación debe mostrar el trabajo del contacto.  <br/> |
|1  <br/> |0x00000003  <br/> |La aplicación debe mostrar la otra dirección del contacto.  <br/> |
|2  <br/> |0x00008080  <br/> |La aplicación debe mostrar Email1.  <br/> |
|2  <br/> |0x00008090  <br/> |La aplicación debe mostrar Email2.  <br/> |
|2  <br/> |0x000080A0  <br/> |La aplicación debe mostrar Email3.  <br/> |
|3,4,5,6  <br/> |PropertyID de cualquiera de las propiedades telefónicas o cualquiera de los números de fax especificados en [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).  <br/> |La aplicación debe mostrar la propiedad correspondiente.  <br/> |
   
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Proporciona definiciones de conjunto de propiedades y referencias a las especificaciones Exchange Server protocolo relacionados.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Especifica las propiedades y las operaciones permitidas para contactos y listas de distribución personales.
    
### <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

