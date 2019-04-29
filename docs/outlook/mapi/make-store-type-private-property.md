---
title: Propiedad de tipo de tienda convertir en privada
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
# <a name="make-store-type-private-property"></a>Propiedad de tipo de tienda convertir en privada

  
  
**Se aplica a**: Outlook 2013 | Outlook 2016 
  
Trata a un almacén secundario como privado.
  
## <a name="quick-info"></a>Información rápida

|||
|:-----|:-----|
|Expuesto el:  <br/> |[IMsgStore: objeto IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Creado por:  <br/> |Proveedor de almacenamiento  <br/> |
|Se obtiene acceso mediante:  <br/> |Outlook y otros clientes  <br/> |
|Tipo de propiedad:  <br/> |PT_BOOLEAN  <br/> |
|Tipo de acceso:  <br/> |Lectura y escritura  <br/> |
   
## <a name="remarks"></a>Comentarios

Para proporcionar cualquiera de las funciones de la tienda, el proveedor de almacenamiento debe implementar [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) y devolver una etiqueta de propiedad válida para cualquiera de estas propiedades pasadas a una llamada a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) . Cuando la etiqueta de propiedad de cualquiera de estas propiedades se pasa a [IMAPIProp:: GetProps](imapiprop-getprops.md), el proveedor de almacén también debe devolver el valor de propiedad correcto. Los proveedores de almacenamiento pueden llamar a [HrGetOneProp](hrgetoneprop.md) y [HrSetOneProp](hrsetoneprop.md) para obtener o establecer estas propiedades. 
  
Para recuperar el valor de esta propiedad, el cliente debe usar primero [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md) para obtener la etiqueta de propiedad y, a continuación, especificar esta etiqueta de propiedad en [IMAPIProp:: GetProps](imapiprop-getprops.md) para obtener el valor. Al llamar a [IMAPIProp:: GetIDsFromNames](imapiprop-getidsfromnames.md), especifique los siguientes valores para la estructura [MAPINAMEID](mapinameid.md) a la que apunta el parámetro de entrada _lppPropNames_:
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind. lpwstrName:  <br/> |L "urn: schemas-microsoft-com: Office: Outlook # storetypeprivate"  <br/> |
   
Un proveedor de almacén puede usar esta propiedad para que Outlook la trate como privada cuando es un almacén secundario de un usuario. 
  
De forma predeterminada, Outlook trata a un almacén secundario de la misma forma que un almacén de delegados, y los elementos del almacén secundario son privados solo si el usuario los marca específicamente como privados. Cuando esta propiedad es **true**, los elementos eliminados de un almacén secundario se mueven a la carpeta **elementos eliminados** en el almacén principal. No se muestran los elementos marcados como privados. Los borradores se almacenan en la carpeta Borradores del almacén principal. 
  
Esta propiedad se omite si la versión de Outlook es anterior a Microsoft Office Outlook 2003 Service Pack 1 o si su valor es **false**.
  

