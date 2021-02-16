---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418095"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica si los Microsoft Office Outlook deben examinar las carpetas de un almacén y archivarlas automáticamente.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Expuesto en:  <br/> |[IMsgStore : IMAPIProp (objeto)](imsgstoreimapiprop.md)  <br/> |
|Creado por:  <br/> |Proveedor de la Tienda  <br/> |
|Acceso mediante:  <br/> |Outlook y otros clientes  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Tipo de acceso:  <br/> |Solo lectura o lectura y escritura según el proveedor de la tienda  <br/> |
   
## <a name="remarks"></a>Comentarios

Para proporcionar cualquiera de las funciones del almacén, el proveedor del almacén debe implementar [IMAPIProp : IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades pasadas a una llamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor del almacén también debe devolver el valor de propiedad correcto. Los proveedores de almacén [pueden llamar a HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades. 
  
Para recuperar el valor de esta propiedad, el cliente primero debe usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor. Al llamar [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) apuntada por el parámetro de entrada  _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"ArchiveSourceSupportMask"  <br/> |
   
Esta propiedad permite a los proveedores de almacenamiento especificar si Outlook debe examinar las carpetas de un almacén y archivarlas automáticamente.
  
De forma predeterminada, esta propiedad no se expone en un almacén, lo que significa que Outlook puede examinar las carpetas del almacén. Si se expone la propiedad, los valores posibles son los siguientes:
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook puede examinar las carpetas del almacén.
    
ASM_DO_NOT_ARCHIVE
  
- Outlook no debe examinar las carpetas del almacén.
    
ASM_CLIENT_DO_NOT_CHANGE
  
- No permita que los clientes cambien esta propiedad en el almacén. Tenga en cuenta que **la ASM_CLIENT_DO_NOT_CHANGE** es para referencia futura y no está implementada actualmente. Por ahora, un almacén puede impedir que los clientes cambien esta marca mediante la configuración del valor que devuelve el almacén para esta propiedad. 
    

