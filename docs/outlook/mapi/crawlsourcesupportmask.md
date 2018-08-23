---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: cc8ff946081fb7817f0f6018acefbe31293a13a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581779"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica si Microsoft Office Outlook debe examinar las carpetas de un almacén, incluidas las carpetas de contactos, calendario y tareas, en Inicio para rellenar el panel de navegación.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Expuesto en:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) objeto  <br/> |
|Creado por:  <br/> |Proveedor de almacenamiento  <br/> |
|Tener acceso a ella:  <br/> |Outlook y otros clientes  <br/> |
|Tipo de propiedad:  <br/> |PT_LONG  <br/> |
|Tipo de acceso:  <br/> |Sólo lectura o lectura y escritura según el proveedor de almacenamiento  <br/> |
   
## <a name="remarks"></a>Comentarios

Para proporcionarlas funcionalidades de almacenamiento, debe implementar el proveedor de almacenamiento [IMAPIProp: IUnknown](imapipropiunknown.md) y devolver una etiqueta de propiedad válido para cualquiera de estas propiedades se pasan a una llamada de [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de la propiedad correcta. Los proveedores de almacén pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades. 
  
Para recuperar el valor de esta propiedad, el cliente debe primero usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especifique esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor. Cuando se llama a [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores de la estructura [MAPINAMEID](mapinameid.md) señalado por el parámetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "CrawlSourceSupportMask"  <br/> |
   
Esta propiedad proporciona una manera para los proveedores de almacén especificar si Outlook debe buscar varias carpetas de un almacén. Se usa en el inicio cuando Outlook examina las carpetas existentes en cada almacén abierto para rellenar el panel de **navegación** ; Outlook comprueba la presencia y el valor de esta propiedad en un almacén antes de iniciar el análisis. 
  
De forma predeterminada, esta propiedad no se expone en un repositorio, lo que significa que Outlook puede examinar las carpetas en el almacén. Si la propiedad se expone, los valores posibles son los siguientes:
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- Outlook puede examinar las carpetas en el almacén.
    
CSM_DO_NOT_CRAWL
  
- Outlook no debe examinar las carpetas en el almacén.
    
CSM_CLIENT_DO_NOT_CHANGE
  
- No permitir a los clientes cambiar esta propiedad en el almacén. Tenga en cuenta que la constante **CSM_CLIENT_DO_NOT_CHANGE** es para futuras referencias y no está implementado actualmente. Por ahora, un almacén puede impedir que los clientes cambien esta marca por codificar el valor que devuelve el almacén de esta propiedad. 
    

