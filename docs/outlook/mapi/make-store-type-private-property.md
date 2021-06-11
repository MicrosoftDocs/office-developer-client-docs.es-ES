---
title: Hacer que el tipo de tienda sea propiedad privada
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Última modificación: 09 de marzo de 2015'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: es-ES
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428546"
---
# <a name="make-store-type-private-property"></a>Hacer que el tipo de tienda sea propiedad privada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Trata un almacén secundario como privado.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Expuesto en:  <br/> |[IMsgStore : objeto IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Creado por:  <br/> |Proveedor de la tienda  <br/> |
|Al que se accede mediante:  <br/> |Outlook y otros clientes  <br/> |
|Tipo de propiedad:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acceso:  <br/> |Lectura/escritura  <br/> |
   
## <a name="remarks"></a>Comentarios

Para proporcionar cualquiera de las funciones del almacén, el proveedor del almacén debe implementar [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades pasadas a una llamada [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp::GetProps](imapiprop-getprops.md), el proveedor de almacenamiento también debe devolver el valor de propiedad correcto. Los proveedores de almacenamiento [pueden llamar a HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp para](hrsetoneprop.md) obtener o establecer estas propiedades. 
  
Para recuperar el valor de esta propiedad, el cliente primero debe usar [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp::GetProps](imapiprop-getprops.md) para obtener el valor. Al llamar [a IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) apuntada por el parámetro de entrada  _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"  <br/> |
   
Un proveedor de almacenamiento puede usar esta propiedad para Outlook tratarla como privada cuando es un almacén secundario para un usuario. 
  
De forma predeterminada, Outlook trata un almacén secundario del mismo modo que un almacén delegado y los elementos del almacén secundario son privados solo si el usuario los marca específicamente como privados. Cuando esta propiedad es **true,** los elementos eliminados de un almacén secundario se mueven a la **carpeta Elementos eliminados** del almacén principal. Los elementos marcados como privados no se muestran. Los borradores se almacenan en la carpeta Borradores del almacén principal. 
  
Esta propiedad se omite si la versión de Outlook es anterior a Microsoft Office Outlook 2003 Service Pack 1 o si su valor es **false**.
  

