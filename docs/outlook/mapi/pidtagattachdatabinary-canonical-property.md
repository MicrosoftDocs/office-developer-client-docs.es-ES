---
title: Propiedad canónica PidTagAttachDataBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachDataBinary
api_type:
- HeaderDef
ms.assetid: 3b0a8b28-863e-4b96-a4c0-fdb8f40555b9
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 1a5f8688b8ea747590cf2a2d6d5efb271aa488f8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356549"
---
# <a name="pidtagattachdatabinary-canonical-property"></a>Propiedad canónica PidTagAttachDataBinary

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Contiene datos adjuntos binarios a los que normalmente se accede a través de la interfaz **IStream** de vinculación e inserción de objetos (OLE). 
  
|||
|:-----|:-----|
|Propiedades asociadas:  <br/> |PR_ATTACH_DATA_BIN  <br/> |
|Identificador:  <br/> |0x3701  <br/> |
|Tipo de datos:  <br/> |PT_BINARY  <br/> |
|Área:  <br/> |Datos adjuntos del mensaje  <br/> |
   
## <a name="remarks"></a>Comentarios

Esta propiedad contiene los datos adjuntos cuando el valor de la propiedad **PR_ATTACH_METHOD** ([PidTagAttachMethod](pidtagattachmethod-canonical-property.md)) es ATTACH_BY_VALUE, que es el método de datos adjuntos habitual y el único necesario para ser compatible. **PR_ATTACH_DATA_BIN** también contiene datos adjuntos OLE 1.0 **OLESTREAM** cuando el valor de **PR_ATTACH_METHOD** es ATTACH_OLE. 
  
 **Los datos adjuntos** olestream se pueden copiar en un archivo llamando al método OLE **IStream::CopyTo.** El tipo de codificación OLE se puede determinar desde **la PR_ATTACH_TAG** ([PidTagAttachTag](pidtagattachtag-canonical-property.md)) propiedad. 
  
Para los datos adjuntos de un archivo de documento OLE, el proveedor del almacén de mensajes debe responder a una llamada [IMAPIProp::OpenProperty](imapiprop-openproperty.md) en **PR_ATTACH_DATA_OBJ** ([PidTagAttachDataObject](pidtagattachdataobject-canonical-property.md)) y puede responder opcionalmente a una llamada en **PR_ATTACH_DATA_BIN**. Tenga en **cuenta que PR_ATTACH_DATA_BIN** y **PR_ATTACH_DATA_OBJ** comparten el mismo identificador de propiedad y, por lo tanto, son dos representaciones de la misma propiedad. 
  
Para un objeto de almacenamiento, como un archivo compuesto en formato docfile OLE 2.0, algunos proveedores de servicios permiten que se abra con la interfaz **IStreamDocfile** MAPI para mejorar el rendimiento. Un proveedor que admite **IStreamDocfile** debe exponerlo en PR_ATTACH_DATA_OBJ y puede exponerlo opcionalmente en **PR_ATTACH_DATA_BIN**.  
  
Para obtener más información sobre las interfaces y formatos [OLE,](https://msdn.microsoft.com/library/d4a57956-37ba-44ca-8efc-bf617ad5e77b.aspx)vea OLE y Transferencia de datos . 
  
## <a name="related-resources"></a>Recursos relacionados

### <a name="protocol-specifications"></a>Especificaciones del protocolo

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Controla objetos de mensaje y datos adjuntos.
    
## <a name="header-files"></a>Archivos de encabezado

Mapidefs.h
  
> Proporciona definiciones de tipo de datos.
    
Mapitags.h
  
> Contiene definiciones de propiedades enumeradas como nombres alternativos.
    
## <a name="see-also"></a>Vea también



[Propiedades MAPI](mapi-properties.md)
  
[Propiedades canónicas MAPI](mapi-canonical-properties.md)
  
[Asignación de nombres de propiedades canónicas a nombres MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Asignación de nombres MAPI a nombres de propiedades canónicas](mapping-mapi-names-to-canonical-property-names.md)

