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
description: '�ltima modificaci�n: lunes, 9 de marzo de 2015'
ms.openlocfilehash: 1e0c099783b4d44b1aaf746b07c77981c135ca9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 06/15/2018
ms.locfileid: "19816441"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**Se aplica a**: Outlook 
  
Especifica si Microsoft Office Outlook debe examinar las carpetas de un almacén y archivarlos automáticamente.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Expuesto en:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto  <br/> |
|Creado por:  <br/> |Proveedor de almacenamiento  <br/> |
|Tener acceso a ella:  <br/> |Outlook y otros clientes  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Tipo de acceso:  <br/> |Sólo lectura o lectura y escritura según el proveedor de almacenamiento  <br/> |
   
## <a name="remarks"></a>Notas

Para proporcionarlas funcionalidades de almacenamiento, debe implementar el proveedor de almacenamiento [IMAPIProp: IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válido para cualquiera de estas propiedades se pasan a una llamada de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de la propiedad correcta. Los proveedores de almacén pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades. 
  
Para recuperar el valor de esta propiedad, el cliente debe primero usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor. Cuando se llama a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores de la estructura [MAPINAMEID](mapinameid.md) señalado por el parámetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "ArchiveSourceSupportMask"  <br/> |
   
Esta propiedad permite que los proveedores de almacén especificar si Outlook debe examinar las carpetas de un almacén y archivarlos automáticamente.
  
De forma predeterminada, esta propiedad no se expone en un repositorio, lo que significa que Outlook puede examinar las carpetas en el almacén. Si la propiedad se expone, los valores posibles son los siguientes:
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook puede examinar las carpetas en el almacén.
    
ASM_DO_NOT_ARCHIVE
  
- Outlook no debe examinar las carpetas en el almacén.
    
ASM_CLIENT_DO_NOT_CHANGE
  
- No permitir a los clientes cambiar esta propiedad en el almacén. Tenga en cuenta que la constante **ASM_CLIENT_DO_NOT_CHANGE** es para futuras referencias y no está implementado actualmente. Por ahora, un almacén puede impedir que los clientes cambien esta marca por codificar el valor que devuelve el almacén de esta propiedad. 
    

