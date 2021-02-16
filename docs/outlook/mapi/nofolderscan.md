---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436814"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Especifica si Microsoft Office Outlook examinar carpetas de contactos en un almacén.
  
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
  
Para recuperar el valor de esta propiedad, el cliente primero debe usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor. Al llamar [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) señalada por el parámetro de entrada  _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"NoFolderScan"  <br/> |
   
Esta propiedad permite a los proveedores de almacenamiento especificar en Outlook que no se deben examinar las carpetas de contactos del almacén para evitar la degradación del rendimiento. Se usa en operaciones de combinación de correspondencia durante las cuales Outlook comprueba la presencia y el valor de esta propiedad antes de iniciar el examen.
  
De forma predeterminada, esta propiedad no se expone en un almacén, lo que significa que Outlook puede examinar la carpeta Contactos del almacén. Si se expone la propiedad, los valores posibles son los siguientes:
  
- Cero (0): Outlook puede llevar a cabo el examen.
    
- Valor distinto de cero: Outlook no debe examinar las carpetas de contactos del almacén.
    

